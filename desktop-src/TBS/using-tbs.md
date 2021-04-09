---
title: Verwenden von TSB
description: Jeder an die TSB gesendete Befehl ist einer bestimmten Entität zugeordnet. Dies wird erreicht, indem ein oder mehrere Kontexte für eine Entität erstellt werden, die dann jedem nachfolgenden von dieser Entität übermittelten Befehl zugeordnet werden.
ms.assetid: 609f1e95-9868-4e34-8758-71306ac4e51f
keywords:
- TDie Basisdienste für TPM, Beispiele
- Basisdienste-TSB von TPM mit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 189d047e6cf969887e390ac7dad1cfc8cdbfa4f9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947765"
---
# <a name="using-tbs"></a>Verwenden von TSB

Die TPM-Basisdienste-Funktion ist in vier Funktionsbereiche unterteilt:

-   [Ressourcenvirtualisierung](resource-virtualization.md)
-   [Befehls Planung](command-scheduling.md)
-   [Energieverwaltung](power-management.md)
-   [Befehls Blockierung](command-blocking.md)

Um sicherzustellen, dass verschiedene Entitäten nicht auf die Ressourcen der anderen zugreifen können, wird jeder an den TSB gesendete Befehl einer bestimmten Entität zugeordnet. Dies wird erreicht, indem ein oder mehrere Kontexte für eine Entität erstellt werden, die dann jedem nachfolgenden von dieser Entität übermittelten Befehl zugeordnet werden. Jeder Befehl enthält ein Kontext Objekt, das es TSB ermöglicht, TPM-Befehle im entsprechenden Kontext auszuführen. Alle durch Befehle erstellten Objekte werden vom TPM geleert, wenn der Kontext geschlossen wird.

Eine Entität erstellt den Kontext, bevor Sie zuerst auf die TSB zugreift und den Kontext verwaltet, bis die TSB-Zugriffe abgeschlossen sind. Im Fall eines TSS würde beispielsweise die TSS-Funktion (TCG Core Services) des TSS einen TSB-Kontext erstellen, wenn er gestartet wird, und diesen Kontext so lange aktiv bleiben, bis er heruntergefahren wird.

Für Windows Server 2008 und Windows Vista schränkt TSB den Zugriff auf die TSB-API für die \\ NetworkService-Konten "Administratoren", "NT Authority LocalService" und "NT Authority" ein \\ . Standardmäßig sind diese Konten die einzigen Konten, mit denen eine Verbindung mit TSB hergestellt und Kontexte erstellt werden können. Zugriffsbeschränkungen können durch Erstellen eines Registrierungsschlüssel **Zugriffs** mit einem Registrierungs Wert Namen für Zeichen folgen (**reg \_ SZ**) **securityDescriptor** geändert werden. <dl> <dt>

Datentyp
</dt> <dd>REG_SZ</dd> </dl> under it as follows:

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         TPM
            Access
               SecurityDescriptor = SecurityDescriptor
```

Beispiel:

**O:Bag: Bad: (A;; 0 x00000001;;; BA) (A;; 0 x00000001;;; NS) (A;; 0 x00000001;;; LS**

Standardmäßig beträgt die maximale Anzahl der von TSB unterstützten Kontexte 25. Diese Nummer kann geändert werden, indem Sie einen **DWORD** -Registrierungs Wert mit dem Namen " **maxkontexte** " unter **HKEY \_ local \_ Machine** \\ **Software** \\ **Microsoft** \\ **TPM** erstellen oder ändern. Die echt Zeitverwendung des TSB-Kontexts kann mithilfe des Leistungs Monitor Tools zum Nachverfolgen der Anzahl von TSB-Kontexten beobachtet werden.

Für Windows 8, Windows Server 2012 und höher, ermöglicht die TSB den Zugriff auf Standardbenutzer und-Administratoren. Die Registrierungsschlüssel **securityDescriptor** und **maxkontexte** wurden als veraltet eingestuft. Für Windows 8, Windows Server 2012 und höher, schränkt TSB den Zugriff auf bestimmte Befehle mithilfe der Befehls Blockierung ein.

Für Windows 10, Version 1607, ermöglicht die TSB den Zugriff von appcontainer-Anwendungen. Für jede TPM-Version wurden die Schlüssel **blockedappcontainercommands** und **AllowedW8AppContainerCommands** mit den entsprechenden Listen der gesperrten bzw. zulässigen TPM-Befehle hinzugefügt.

Für Windows 10, Version 1803, werden die Registrierungsschlüssel unter **AllowedW8AppContainerCommands** nicht mehr unterstützt.

 

 




