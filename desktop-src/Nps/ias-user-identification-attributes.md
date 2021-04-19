---
title: Benutzer Identifizierungs Attribute
description: Die Identität des Benutzers, der die Authentifizierung anfordert, wird für die NPS-Erweiterungs-DLLs in einer Reihe unterschiedlicher Attribute bereitgestellt.
ms.assetid: 2f741a81-e432-47fe-a14a-8b77ecd41e28
ms.tgt_platform: multiple
keywords:
- Attribute, Benutzeridentifikation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 527bdffad376ce92fa2fd7c5d5330fb752fea6aa
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106341739"
---
# <a name="user-identification-attributes"></a>Benutzer Identifizierungs Attribute

> [!Note]  
> Der Internet Authentifizierungsdienst (IAS) wurde ab Windows Server 2008 in den Netzwerk Richtlinien Server (Network Policy Server, NPS) umbenannt. Der Inhalt dieses Themas gilt sowohl für IAS als auch für NPS. Im gesamten Text wird NPS verwendet, um auf alle Versionen des Dienstanbieter zu verweisen, einschließlich der Versionen, die ursprünglich als IAS bezeichnet wurden.

 

Die Identität des Benutzers, der die Authentifizierung anfordert, wird für die NPS-Erweiterungs-DLLs in einer Reihe unterschiedlicher Attribute bereitgestellt.

-   **ratusername**
-   **ratstrippeer Name**
-   **ratsqusername**

Jedes Attribut stellt die Benutzeridentität in einem anderen Format bereit. Im Allgemeinen sollten Entwickler **ratstripetdusername** verwenden. Die Verwendung des **ratusername** -Attributs und des **ratf qusername** -Attributs ist spezialisiertere.

> [!Note]  
> Das User-Password-Attribut, **ratuserpassword**, wurde bereits entschlüsselt, wenn es an die Erweiterungs-DLL gesendet wird und in diesem Formular verwendbar ist.

 

## <a name="ratusername"></a>ratusername

Das **ratusername** -Attribut enthält den Namen, der tatsächlich gesendet wurde. NPS hat den Inhalt dieses Attributs in keiner Weise verarbeitet oder überprüft. Dieses Attribut ist möglicherweise überhaupt nicht verfügbar, da der Benutzer möglicherweise über eine Methode, z. b. eine Aufruferkennung, identifiziert worden ist.

Wenn dieses Attribut verfügbar ist, ist es bei Verwendung von [**radiusextensionprocess/Ex**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_ex)nur im Plug-in-Punkt der Authentifizierungs Erweiterung verfügbar. Das **ratusername** -Attribut ist im Plug-in-Punkt der Autorisierungs Erweiterung nicht verfügbar, da die **radiusextensionprocess/Ex-** Funktionen in Autorisierungs Erweiterungs-DLLs nur die "ausgehenden" Attribute sehen.

Wenn dieses Attribut bei Verwendung von [**RadiusExtensionProcess2**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_2)verfügbar ist, ist es sowohl unter dem Plug-in-Endpunkt der Authentifizierungs Erweiterung als auch im Plug-in-Punkt der Autorisierungs Erweiterung verfügbar.

## <a name="ratstrippedusername"></a>ratstrippeer Name

" **Ratstripetdusername** " ist die Identität des Benutzers nach "Bereichs Einschränkung". Weitere Informationen zum Entfernen von Bereichen finden Sie im Thema " [Bereichs Namen](/previous-versions/windows/it-pro/windows-server-2003/cc779938(v=ws.10)) " unter http: \\ \\ technet2.Microsoft.com.

Dieses Attribut ist möglicherweise im Plug-in-Endpunkt der Authentifizierungs Erweiterung, dem Plug-in-Endpunkt für die Autorisierungs Erweiterung oder beides vorhanden. Dieses Attribut weist garantiert folgendes Format auf:

*Domänen ***\\*** Benutzername*

Dabei ist *Domäne* der NetBIOS-Domänen Name.

## <a name="ratfqusername"></a>ratsqusername

Das **ratfqusername** -Attribut ist der "voll qualifizierte" Benutzername.

Dieses Attribut ist möglicherweise im Plug-in-Endpunkt der Authentifizierungs Erweiterung, dem Plug-in-Endpunkt für die Autorisierungs Erweiterung oder beides vorhanden. Allerdings kann sich das Format des-Attributs zwischen den beiden Plug-in-Punkten unterscheiden. Beim Plug-in-Plug-in für Authentifizierungs Erweiterungen weist dieses Attribut immer folgendes Format auf:

*Domänen ***\\*** Benutzername*

Das Format des **ratsqusername** -Attributs am Plug-in-Punkt der Autorisierungs Erweiterung ist davon abhängig, ob der Benutzer ein Active Directory Benutzer ist.

-   Wenn es sich bei dem Benutzer um einen lokalen Benutzer handelt **, hat das** gleiche Format wie für den Plug-in-Endpunkt der Authentifizierungs Erweiterungs-DLL:

    *Domänen ***\\*** Benutzername*

    .

-   Wenn der Benutzer ein Active Directory Benutzer ist, kann " **ratsqusername** " den Namen des Benutzers im "kanonischen" Format enthalten. Das kanonische Format ist das Format, das vom Active Directory verwendet wird, um den Benutzer zu identifizieren. Dabei handelt es sich um den Pfad aus dem Stammverzeichnis der Active Directory Struktur, der die Organisationseinheit (OU) des Benutzers enthält.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Einrichten der Erweiterungs-DLLs](/windows/desktop/Nps/ias-setting-up-the-extension-and-authorization-dlls)
</dt> <dt>

[Aufrufen der Erweiterungs-DLLs](/windows/desktop/Nps/ias-authentication-and-authorization-process)
</dt> </dl>

 

 