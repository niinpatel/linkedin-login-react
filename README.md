# linkedin-login-for-react

    npm install linkedin-login-for-react

**Sample Use**

    import React from 'react'
    import LinkedIn from 'linkedin-login-for-react'
    import styles from './styles.css'

    class LoginWithLinkedin extends React.Component {

    static propTypes = {

    }

    /*
    ** @code = authorization code from linkedin api
    ** @redirectUri = redirect uri from linkedin api
    ** @error = error message sign in failed
    */
    callbackLinkedIn = (error, code, redirectUri) => {
        if(error){
            // signin failed
        } else {
            // Obtain authorization token from linkedin api
            // see https://developer.linkedin.com/docs/oauth2 for more info
        }
    }

    render () {
    return (
    <LinkedIn
            clientId='xxx'
            callback={this.callbackLinkedIn}
            className={styles.linkedin}
            text='Login With LinkedIn' />
    )
    }

    }

    export default LoginWithLinkedin
