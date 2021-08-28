---
title: Benutzeridentifikationsattribute
description: Die Identität des Benutzers, der die Authentifizierung anfordert, wird den NPS-Erweiterungs-DLLs in einer Reihe verschiedener Attribute bereitgestellt.
ms.assetid: 2f741a81-e432-47fe-a14a-8b77ecd41e28
ms.tgt_platform: multiple
keywords:
- Attribute, Benutzeridentifikation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff099b46844f2259ad127346bb1ee2bfafccf4b116f3dba86dff3e175d11c28c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120128760"
---
# <a name="user-identification-attributes"></a>Benutzeridentifikationsattribute

> [!Note]  
> Der Internetauthentifizierungsdienst (INTERNET Authentication Service, IAS) wurde ab Windows Server 2008 in Netzwerkrichtlinienserver (Network Policy Server, NPS) umbenannt. Der Inhalt dieses Themas gilt sowohl für IAS als auch für NPS. Im gesamten Text wird NPS verwendet, um auf alle Versionen des Diensts zu verweisen, einschließlich der Versionen, die ursprünglich als IAS bezeichnet wurden.

 

Die Identität des Benutzers, der die Authentifizierung anfordert, wird den NPS-Erweiterungs-DLLs in einer Reihe verschiedener Attribute bereitgestellt.

-   **ratUserName**
-   **ratStrippedUserName**
-   **ratFQUserName**

Jedes Attribut stellt die Benutzeridentität in einem anderen Format bereit. Im Allgemeinen sollten Entwickler **ratStrippedUserName** verwenden. Die Verwendungsmöglichkeiten der Attribute **ratUserName** und **ratFQUserName sind spezialisierter.**

> [!Note]  
> Das User-Password-Attribut **ratUserPassword** wurde beim Senden an die Erweiterungs-DLL bereits entschlüsselt und kann in dieser Form verwendet werden.

 

## <a name="ratusername"></a>ratUserName

Das **ratUserName-Attribut** enthält den Namen, der tatsächlich "über das Kabel" gesendet wurde. NPS hat den Inhalt dieses Attributs in keiner Weise verarbeitet oder überprüft. Dieses Attribut ist möglicherweise überhaupt nicht verfügbar, da der Benutzer möglicherweise über ein Mittel wie die Aufrufer-ID identifiziert wurde.

Wenn [**Sie RadiusExtensionProcess/Ex**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_ex)verwenden, ist dieses Attribut nur am DLL-Plug-In-Punkt der Authentifizierungserweiterung verfügbar, wenn dieses Attribut verfügbar ist. Das **ratUserName-Attribut** ist am DLL-Plug-In-Punkt der Autorisierungserweiterung nicht verfügbar, da die **RadiusExtensionProcess/Ex-Funktionen** in Autorisierungserweiterungs-DLLs nur die "ausgehenden" Attribute sehen.

Wenn [**Sie RadiusExtensionProcess2**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_2)verwenden, ist dieses Attribut sowohl am DLL-Plug-In-Punkt der Authentifizierungserweiterung als auch am DLL-Plug-In-Punkt für die Autorisierungserweiterung verfügbar.

## <a name="ratstrippedusername"></a>ratStrippedUserName

**RatStrippedUserName** ist die Identität des Benutzers nach dem Bereichsstripping. Weitere Informationen zum Bereichsstripping finden Sie im Thema [Bereichsnamen](/previous-versions/windows/it-pro/windows-server-2003/cc779938(v=ws.10)) unter http: \\ \\ technet2.microsoft.com.

Dieses Attribut kann am DLL-Plug-In-Punkt der Authentifizierungserweiterung, am DLL-Plug-In-Punkt für die Autorisierungserweiterung oder in beiden vorhanden sein. Dieses Attribut hat garantiert das folgende Format:

*Domain* **\\** _UserName_

Wobei *Domäne* der NetBIOS-Domänenname ist.

## <a name="ratfqusername"></a>ratFQUserName

Das **ratFQUserName-Attribut** ist der vollqualifizierte Benutzername.

Dieses Attribut kann im Dll-Plug-In-Punkt der Authentifizierungserweiterung, im Dll-Plug-In-Punkt für die Autorisierungserweiterung oder in beiden vorhanden sein. Das Format des Attributs kann sich jedoch zwischen den beiden Plug-In-Punkten unterscheiden. Am Dll-Plug-In-Punkt der Authentifizierungserweiterung hat dieses Attribut immer folgendes Format:

*Domain* **\\** _UserName_

Das Format des **ratFQUserName-Attributs** am DLL-Plug-In-Punkt der Autorisierungserweiterung hängt davon ab, ob der Benutzer ein Active Directory-Benutzer ist.

-   Wenn der Benutzer ein lokaler Benutzer ist, weist **ratFQUserName** das gleiche Format wie für den DLL-Plug-In-Punkt der Authentifizierungserweiterung auf:

    *Domain* **\\** _UserName_

    .

-   Wenn der Benutzer ein Active Directory-Benutzer ist, kann **ratFQUserName** den Namen des Benutzers im kanonischen Format enthalten. Das kanonische Format ist das Format, das von Active Directory zum Identifizieren des Benutzers verwendet wird. Dies ist der Pfad aus dem Stamm der Active Directory-Struktur und enthält die Organisationseinheit (OE) des Benutzers.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Einrichten der Erweiterungs-DLLs](/windows/desktop/Nps/ias-setting-up-the-extension-and-authorization-dlls)
</dt> <dt>

[Aufrufen der Erweiterungs-DLLs](/windows/desktop/Nps/ias-authentication-and-authorization-process)
</dt> </dl>

 

 