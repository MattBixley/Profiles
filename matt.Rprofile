### matt.Rprofile
local({r <- getOption("repos")
      r["CRAN"] <- "http://cran.stat.auckland.ac.nz/"
      options(repos=r)})

#############
## OPTIONS ##
#############

# c'mon now
options(stringsAsFactors=FALSE)

options(max.print=100)

options(scipen=100)

options(editor="nano")

# ain't nobody got time for Tk to load
options(menu.graphics=FALSE)

# the non-standard continuation prompt
# helps me tell when I accidentally fail
# to close a paren, etc..
options(prompt="> ")
options(continue="...+ ")

# tab-complete package names
utils::rc.settings(ipck=TRUE)

.First <- function(){
  if(interactive()){
    library(utils)
    # puts a timestamp in my command history
    # file if R_HISTFILE is in environment
    timestamp(,prefix=paste("##------ [",getwd(),"] ",sep=""))

  }
}

# get pretty output colors in the terminal
if(Sys.getenv("TERM") == "xterm-256color")
  library("colorout")

# get noisy package imports to shut up
#   we have to jump through hoops to get the
#   call to "library()" to work because it
#   will try to load a package even if it is not
#   a string literal
sshhh <- function(a.package){
  suppressWarnings(suppressPackageStartupMessages(
    library(a.package, character.only=TRUE)))
}

# list of packages to auto-load if interactive
auto.loads <-c("tidyverse", "magrittr", "assertr","usethis","devtools")

# auto-load dplyr and ggplot2
if(interactive()){
  invisible(sapply(auto.loads, sshhh))
}

## .First() run at the start of every R session. 
## Use to load commonly used packages? 
.First <- function() {
	cat("\nSuccessfully loaded .Rprofile at", date(), "\n")
}

## .Last() run at the end of the session
.Last <- function() {
	# save command history here?
	cat("\nGoodbye at ", date(), "\n")
}

if (requireNamespace("prompt", quietly = TRUE)) {
  prompt_git <- function(...) {
    paste0(
      "[", prompt::git_branch(), "]",
      " > "
    )
  }
  prompt::set_prompt(prompt_git)
  rm(prompt_git)
}

if (interactive()) {
  suppressMessages(require(devtools))
  suppressMessages(require(usethis))
  suppressMessages(require(testthat))
}

options(
  warnPartialMatchArgs = TRUE,
  warnPartialMatchDollar = TRUE,
  warnPartialMatchAttr = TRUE
)

### matt.Rprofile
local({r <- getOption("repos")
      r["CRAN"] <- "https://cran.stat.auckland.ac.nz/"
      options(repos=r)})

#############
## OPTIONS ##
#############

# c'mon now
options(stringsAsFactors=FALSE)

options(max.print=100)

options(scipen=15)

options(editor="nano")

# ain't nobody got time for Tk to load
options(menu.graphics=FALSE)

# the non-standard continuation prompt
# helps me tell when I accidentally fail
# to close a paren, etc..
options(prompt="> ")
options(continue="...+ ")

# tab-complete package names
utils::rc.settings(ipck=TRUE)

.First <- function(){
  if(interactive()){
    library(utils)
    # puts a timestamp in my command history
    # file if R_HISTFILE is in environment
    timestamp(,prefix=paste("##------ [",getwd(),"] ",sep=""))
  }
}

## .First() run at the start of every R session. 
## Use to load commonly used packages? 
.First <- function() {
        cat("\nSuccessfully loaded Matts .Rprofile at", date(), "\n")
}

## .Last() run at the end of the session
.Last <- function() {
        # save command history here?
        cat("\nGoodbye at ", date(), "\n")
}


.toggle <- function(){
  # Assumes you are in user mode if first time running in session
  rstudioTeachMode_options <-  getOption("rstudioTeachMode")
  if (is.null(rstudioTeachMode_options)) rstudioTeachMode_options <- list(mode = "user")
  # teach -> user
  if (rstudioTeachMode_options$mode == "teach") {
    # select what you want your user settings to be here
    rstudioapi::writeRStudioPreference("font_size_points", 11L) # number has to be integer
    rstudioapi::applyTheme("Cobalt")
  } else {# user -> teach
    # select what you want your teaching settings to be
    rstudioapi::writeRStudioPreference("font_size_points", 24L) # number has to be integer
    rstudioapi::applyTheme("Chrome")
  }
  # flip the mode in the stored options
  rstudioTeachMode_options$mode <- ifelse(rstudioTeachMode_options$mode == "teach", "user", "teach")
  options(rstudioTeachMode = rstudioTeachMode_options)
}


.toggle <- function(){
  # Assumes you are in user mode if first time running in session
  rstudioTeachMode_options <-  getOption("rstudioTeachMode")
  if (is.null(rstudioTeachMode_options)) rstudioTeachMode_options <- list(mode = "user")
  # teach -> user
  if (rstudioTeachMode_options$mode == "teach") {
    # select what you want your user settings to be here
    rstudioapi::writeRStudioPreference("font_size_points", 11L) # number has to be integer
    rstudioapi::applyTheme("Cobalt")
  } else {# user -> teach
    # select what you want your teaching settings to be
    rstudioapi::writeRStudioPreference("font_size_points", 24L) # number has to be integer
    rstudioapi::applyTheme("Chrome")
  }
  # flip the mode in the stored options
  rstudioTeachMode_options$mode <- ifelse(rstudioTeachMode_options$mode == "teach", "user", "teach")
  options(rstudioTeachMode = rstudioTeachMode_options)
}
