---
title: Authentifizierung (Windows Media Format 11 SDK)
description: Authentifizierung
ms.assetid: 9c181615-e864-4588-846f-d04d73824f5f
keywords:
- Windows Medienformat-SDK, Authentifizierung
- Windows Medienformat-SDK, Netzwerkauthentifizierung
- Advanced Systems Format (ASF), Authentifizierung
- ASF (Advanced Systems Format), Authentifizierung
- Advanced Systems Format (ASF), Netzwerkauthentifizierung
- ASF (Advanced Systems Format), Netzwerkauthentifizierung
- authentication
- Netzwerkauthentifizierung,Informationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ee276bc2800ad7f2d5fa94f00e282dc7d4f5402396d69eb7e3b240fd4303f4b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120007120"
---
# <a name="authentication-windows-media-format-11-sdk"></a>Authentifizierung (Windows Media Format 11 SDK)

Das Readerobjekt kann Herausforderungen bei der Netzwerkauthentifizierung behandeln, einschließlich Digestauthentifizierung und NTLM-Authentifizierung. In einigen Fällen muss die Anwendung die Anmeldeinformationen des Benutzers über eine Rückrufschnittstelle bereitstellen:

-   Digestauthentifizierung: Die Anwendung muss die **IWMCredentialCallback-Schnittstelle** implementieren, wie weiter unten in diesem Thema beschrieben.
-   NTLM-Authentifizierung: Der Reader antwortet automatisch mit den Anmeldeinformationen des Benutzers. Wenn der aktuelle Benutzer autorisiert ist, sich beim Server anmelden, muss die Anwendung nichts tun. Wenn der Benutzer keine Autorisierung hat, muss die Anwendung die **IWMCredentialCallback-Schnittstelle** implementieren.

    > [!Note]  
    > Windows Media-Dienste Version 4.1 unterstützt keine NTLM-Authentifizierung über einen Proxyserver. Die NTLM-Authentifizierung erfordert mehrere Client-Server-Austauschprogramme über dieselbe Verbindung, und Version 4.1 hält keine permanente Verbindung mit dem Proxy. Windows Media-Dienste 9-Serie in Microsoft Windows Server 2003 unterstützt die NTLM-Authentifizierung über einen Proxyserver, solange der Proxy Keep-Alive-Verbindungen unterstützt.

     

Wie bereits erwähnt, muss die Anwendung in einigen Fällen die Anmeldeinformationen des Benutzers bereitstellen. Dies erfolgt über die **IWMCredentialCallback-Schnittstelle,** die über eine einzelne **AcquireCredentials-Methode verfügt.** Implementieren Sie diese Schnittstelle in Ihrer Anwendung, um die Authentifizierung zu unterstützen. Das Readerobjekt fragt diese Schnittstelle ab, indem **es QueryInterface** für den [**IWMReaderCallback-Zeiger**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadercallback) aufruft, den es von der Anwendung in der [**IWMReader::Open-Methode empfangen**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open) hat. Wenn das Readerobjekt die Anmeldeinformationen des Benutzers erhalten muss, ruft es die **AcquireCredentials-Methode der Anwendung** auf.

Wenn die Anmeldeinformationen ohne Verschlüsselung über das Netzwerk gesendet werden, legt der Reader das WMT \_ CREDENTIAL \_ CLEAR TEXT-Flag im parameter \_ *pdwFlags* fest. Dies gibt der Anwendung die Möglichkeit, den Benutzer zu warnen, dass seine Anmeldeinformationen als Nur-Text gesendet werden.

Andernfalls verschlüsselt das Readerobjekt die Anmeldeinformationen automatisch, bevor sie über das Netzwerk übertragen werden. Die Anwendung kann sie als Nur-Text an das Readerobjekt zurückgeben. Wenn das Readerobjekt das WMT CREDENTIAL ENCRYPT-Flag fest legt, bedeutet dies außerdem, dass der Leser das Abrufen verschlüsselter Anmeldeinformationen \_ \_ von der Anwendung unterstützt. In diesem Fall kann die Anwendung die Anmeldeinformationen entweder im Nur-Text-Text zurückgeben oder sie selbst mithilfe der **CryptProtectData-Funktion** verschlüsseln, die in der Dokumentation zum Platform SDK beschrieben wird. Wenn die Anwendung die Anmeldeinformationen verschlüsselt, muss sie das WMT \_ CREDENTIAL \_ ENCRYPT-Flag im *pdwFlags-Parameter* festlegen, bevor die Methode zurückgegeben wird.

Im Allgemeinen ist es nicht erforderlich, die Daten zu verschlüsseln, da das Readerobjekt die Daten bei Bedarf verschlüsselt. Die Verschlüsselung kann jedoch nützlich sein, wenn die Anwendung den Benutzernamen und das Kennwort im Arbeitsspeicher speichert, da sie einen Angreifer daran hindert, ein Speicherabbild des Prozesses zu überprüfen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**IWMCredentialCallback-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcredentialcallback)
</dt> <dt>

[**IWMReader-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader)
</dt> </dl>

 

 




