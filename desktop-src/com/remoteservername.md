---
title: RemoteServerName
description: Konfiguriert den Client so, dass das Objekt auf einem bestimmten Computer ausgeführt wird, wenn eine Aktivierungsfunktion aufgerufen wird, für die keine COSERVERINFO-Struktur angegeben ist.
ms.assetid: 0413564e-e8ba-4e6e-ad29-62997c63aab3
keywords:
- Remoteservername-Registrierungs Wert com
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0634d858b04fbbdf5d3a6024dbd9fdea4ee06d99
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "106339918"
---
# <a name="remoteservername"></a>RemoteServerName

Konfiguriert den Client so, dass das Objekt auf einem bestimmten Computer ausgeführt wird, wenn eine Aktivierungsfunktion aufgerufen wird, für die keine [**COSERVERINFO**](/windows/win32/api/objidlbase/ns-objidlbase-coserverinfo) -Struktur angegeben ist.

## <a name="registry-entry"></a>Registrierungseintrag

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      RemoteServerName = name
```

## <a name="remarks"></a>Bemerkungen

**Remoteservername** ermöglicht die einfache Konfigurations Verwaltung von Client Anwendungen. Sie können ohne hart codierte Servernamen geschrieben werden und können konfiguriert werden, indem Sie die **Remoteservername** -Registrierungs Werte der Klassen von Objekten ändern, die Sie verwenden.

Wie in der Dokumentation für die [**CLSCTX**](/windows/win32/api/wtypesbase/ne-wtypesbase-clsctx) -Enumeration und die [**COSERVERINFO**](/windows/win32/api/objidlbase/ns-objidlbase-coserverinfo) -Struktur beschrieben, handelt es sich bei einem der Parameter der verteilten COM-Aktivierung um einen Zeiger auf eine **COSERVERINFO** -Struktur. Wenn dieser Wert nicht **null** ist, überschreibt die Informationen in der **COSERVERINFO** -Struktur die Einstellung des **Remoteservername** -Schlüssels für den Funktions Aufruf.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Registrieren von com-Servern](registering-com-servers.md)
</dt> </dl>

 

 