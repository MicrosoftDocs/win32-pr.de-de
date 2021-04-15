---
title: Asynchroner und synchroner Speicher
description: Asynchroner und synchroner Speicher
ms.assetid: de8c50f8-1733-439f-ab53-f98ac21a1fae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 884b8613bebf8ef401f76e4761f48fa0ddd831c2
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104517159"
---
# <a name="asynchronous-and-synchronous-storage"></a>Asynchroner und synchroner Speicher

Asynchrone Moniker können auch ein [asynchrones Speicher](/windows/desktop/Stg/asynchronous-storage) Objekt in der [**ibindstatus-Rückruf:: ondataavailable**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775061(v=vs.85)) -Benachrichtigung zurückgeben. Dieses Speicher Objekt erlaubt möglicherweise den Zugriff auf einige der persistenten Daten des Objekts, während die Bindung noch läuft. Ein Client kann zwischen zwei Modi für den Speicher wählen: Blockierung und nicht Blockierung.

Im Blockierungs Modus, der mit aktuellen Implementierungen von Speicher Objekten kompatibel ist, wird der-Befehl so lange blockiert, bis Daten empfangen werden, wenn Daten nicht verfügbar sind. Im nicht blockierenden Modus gibt das Speicher Objekt einen neuen Fehler zurück, der \_ ausstehend ist, wenn Daten nicht verfügbar sind. Ein Client, der die asynchrone Bindung und den Speicher kennt, bemerkt diesen Fehler und wartet auf weitere Benachrichtigungen ([**ondataavailable**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775061(v=vs.85))), um den Vorgang zu wiederholen. Ein Client kann zwischen einem synchronen (blockierenden) und asynchronen (nicht blockierenden) Speicher wählen, indem er entscheidet, ob das bindf \_ asyncstorage-Flag im *grfbindf* -Wert festgelegt wird, der an [**IBindStatusCallback:: getbindinfo**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775058(v=vs.85))zurückgegeben wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Asynchrone Moniker](asynchronous-monikers.md)
</dt> </dl>

 

 