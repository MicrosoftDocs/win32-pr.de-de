---
title: Authentifizierung (AD DS)
description: Jedes Objekt in Active Directory Domain Services verfügt über eine eindeutige Sicherheits Beschreibung, die die Zugriffsberechtigungen definiert, die erforderlich sind, um das Objekt oder seine individuellen Eigenschaften zu lesen oder zu aktualisieren.
ms.assetid: a4a663d3-b0f3-4993-a74e-9e4f896e8c95
ms.tgt_platform: multiple
keywords:
- Active Directory, verwenden, Bindung, Authentifizierung
- Binden der Authentifizierungs Anzeige
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb80bbca4604a99011d3198eaf6b3e871cd3f84c
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "104472700"
---
# <a name="authentication-ad-ds"></a>Authentifizierung (AD DS)

Jedes Objekt in Active Directory Domain Services verfügt über eine eindeutige Sicherheits Beschreibung, die die Zugriffsberechtigungen definiert, die erforderlich sind, um das Objekt oder seine individuellen Eigenschaften zu lesen oder zu aktualisieren. Zugriffsberechtigungen werden durch die Rechte festgelegt, die für das Konto oder die Gruppenmitgliedschaften eines Benutzers erteilt wurden.

Wenn eine Anwendung an ein Objekt im Verzeichnis gebunden wird, basieren die Zugriffsrechte, die die Anwendung auf dieses Objekt hat, auf dem Benutzer Kontext, der während des Bindungs Vorgangs angegeben wurde. Für die Bindungsfunktionen und-Methoden [**ADsGetObject**](/windows/desktop/api/adshlp/nf-adshlp-adsgetobject), [**ADsOpenObject**](/windows/desktop/api/adshlp/nf-adshlp-adsopenobject), **GetObject**, [**iadsopendsobject:: opendsobject**](/windows/desktop/api/iads/nf-iads-iadsopendsobject-opendsobject)kann eine Anwendung implizit die Anmelde Informationen des Aufrufers verwenden, die Anmelde Informationen eines Benutzerkontos explizit angeben oder einen nicht authentifizierten Benutzer Kontext (Guest) verwenden.

 

 