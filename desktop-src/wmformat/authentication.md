---
title: Authentifizierung (Windows Media-Format 11 SDK)
description: Authentifizierung
ms.assetid: 9c181615-e864-4588-846f-d04d73824f5f
keywords:
- SDK für Windows Media-Format, Authentifizierung
- Windows Media-Format-SDK, Netzwerk Authentifizierung
- Advanced Systems Format (ASF), Authentifizierung
- ASF (Advanced Systems Format), Authentifizierung
- Advanced Systems Format (ASF), Netzwerk Authentifizierung
- ASF (Advanced Systems Format), Netzwerk Authentifizierung
- authentication
- Netzwerk Authentifizierung, Informationen zu
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0bf815881ac7beb354fffbfdb9b5475d040e9e83
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "106338516"
---
# <a name="authentication-windows-media-format-11-sdk"></a>Authentifizierung (Windows Media-Format 11 SDK)

Das Reader-Objekt kann Probleme mit der Netzwerk Authentifizierung behandeln, einschließlich Digestauthentifizierung und NTLM-Authentifizierung. In einigen Fällen muss die Anwendung die Anmelde Informationen des Benutzers über eine Rückruf Schnittstelle bereitstellen:

-   Digestauthentifizierung: die Anwendung muss die **iwmkredentialcallback** -Schnittstelle implementieren, wie weiter unten in diesem Thema beschrieben.
-   NTLM-Authentifizierung: der Reader antwortet automatisch mit den Anmelde Informationen des Benutzers. Wenn der aktuelle Benutzer für die Anmeldung am Server autorisiert ist, muss die Anwendung nichts Unternehmen. Wenn der Benutzer keine Autorisierung hat, muss die Anwendung die **iwmkredentialcallback** -Schnittstelle implementieren.

    > [!Note]  
    > Windows Media Services Version 4,1 unterstützt die NTLM-Authentifizierung nicht über einen Proxy Server. Die NTLM-Authentifizierung erfordert mehrere Client/Server-Austausch Vorgänge auf derselben Verbindung, und Version 4,1 behält keine permanente Verbindung mit dem Proxy bei. Die Windows Media Services 9-Reihe in Microsoft Windows Server 2003 unterstützt die NTLM-Authentifizierung über einen Proxy Server, solange der Proxy Keep-Alive-Verbindungen unterstützt.

     

Wie bereits erwähnt, muss die Anwendung in einigen Fällen die Anmelde Informationen des Benutzers bereitstellen. Dies erfolgt über die **iwmkredentialcallback** -Schnittstelle, die über eine einzige Methode ( **acquirecredenseins**) verfügt. Implementieren Sie diese Schnittstelle in der Anwendung, um die Authentifizierung zu unterstützen. Das Reader-Objekt fragt diese Schnittstelle ab, indem **QueryInterface** für den [**iwmreadercallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadercallback) -Zeiger aufgerufen wird, der von der Anwendung in der [**iwmreader:: Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open) -Methode empfangen wurde. Wenn das Reader-Objekt die Anmelde Informationen des Benutzers erhalten muss, ruft es die **acquirecreden-** Methode der Anwendung auf.

Wenn die Anmelde Informationen ohne Verschlüsselung über das Netzwerk gesendet werden, legt der Reader das Flag zum Löschen von WMT-Anmelde Informationen \_ \_ \_ im *pdwflags* -Parameter fest. Dadurch erhält die Anwendung die Möglichkeit, den Benutzer zu warnen, dass Ihre Anmelde Informationen als nur-Text gesendet werden.

Andernfalls werden die Anmelde Informationen automatisch vom Reader-Objekt verschlüsselt, bevor Sie über das Netzwerk gesendet werden. Die Anwendung kann Sie als Klartext an das Reader-Objekt zurückgeben. Wenn das Reader-Objekt das Flag zum Verschlüsseln der WMT-Anmelde Informationen festlegt \_ \_ , bedeutet dies, dass der Reader das erhalten verschlüsselter Anmelde Informationen aus der Anwendung unterstützt. In diesem Fall kann die Anwendung die Anmelde Informationen entweder im nur-Text-Modus zurückgeben oder Sie selbst mithilfe der **CryptProtectData** -Funktion verschlüsseln, die in der Platform SDK-Dokumentation beschrieben wird. Wenn die Anwendung die Anmelde Informationen verschlüsselt, muss Sie das Flag für die WMT-Anmelde Informationen \_ \_ Verschlüsselung im *pdwflags* -Parameter festlegen, bevor die Methode zurückgegeben wird.

Im Allgemeinen ist es nicht notwendig, die Daten zu verschlüsseln, da das Reader-Objekt die Daten bei Bedarf verschlüsselt. Die Verschlüsselung kann jedoch nützlich sein, wenn die Anwendung den Benutzernamen und das Kennwort im Arbeitsspeicher beibehält, da Sie verhindert, dass ein Angreifer ein Speicher Abbild des Prozesses überprüft.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Iwmkredentialcallback-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcredentialcallback)
</dt> <dt>

[**Iwmreader-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader)
</dt> </dl>

 

 




