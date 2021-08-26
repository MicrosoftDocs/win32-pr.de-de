---
title: Asynchrone und synchrone Storage
description: Asynchrone und synchrone Storage
ms.assetid: de8c50f8-1733-439f-ab53-f98ac21a1fae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a5662f5d9291de19fb39f044731ed72fd1db2cb04fe29d76eb785981ddeb8a9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120071090"
---
# <a name="asynchronous-and-synchronous-storage"></a>Asynchrone und synchrone Storage

Asynchrone Moniker geben möglicherweise auch ein [Asynchronous Storage-Objekt](/windows/desktop/Stg/asynchronous-storage) in der [**IBindStatusCallback::OnDataAvailable-Benachrichtigung**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775061(v=vs.85)) zurück. Dieses Speicherobjekt ermöglicht möglicherweise den Zugriff auf einige der persistenten Daten des Objekts, während die Bindung noch in Bearbeitung ist. Ein Client kann zwischen zwei Modi für den Speicher wählen: blockierend und nicht blockierend.

Im Blockierungsmodus, der mit aktuellen Implementierungen von Speicherobjekten kompatibel ist, wird der Aufruf blockiert, bis Daten eintreffen, wenn keine Daten verfügbar sind. Im Nichtblockierungsmodus gibt das Speicherobjekt den neuen Fehler E AUSSTEHENd zurück, wenn keine Daten verfügbar sind, anstatt den \_ Aufruf zu blockieren. Ein Client, der die asynchrone Bindung und den Speicher kennt, notiert diesen Fehler und wartet auf weitere Benachrichtigungen ([**OnDataAvailable**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775061(v=vs.85))), um den Vorgang erneut zu versuchen. Ein Client kann zwischen einem synchronen (blockierenden) und asynchronen (nicht blockierenden) Speicher wählen, indem er auswählt, ob das BINDF ASYNCSTORAGE-Flag in dem grfBINDF-Wert festgelegt werden soll, der an \_ [**IBindStatusCallback::GetBindInfo**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775058(v=vs.85))zurückgegeben wird. 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Asynchrone Moniker](asynchronous-monikers.md)
</dt> </dl>

 

 