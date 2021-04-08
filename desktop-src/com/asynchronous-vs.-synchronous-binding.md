---
title: Asynchrone und synchrone Bindung
description: Asynchrone und synchrone Bindung
ms.assetid: 9852df19-5ae4-4425-9ce0-cac160d68456
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11b022df239221f0a019b972067248225210e585
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "103730520"
---
# <a name="asynchronous-and-synchronous-binding"></a>Asynchrone und synchrone Bindung

Der Client kann überprüfen, ob der Moniker asynchron ist, indem er die [**isasyncmoniker**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775110(v=vs.85)) -Funktion aufrufen. Wenn der Client das asynchrone bindf-Flag zurückgibt \_ , anstatt einen Objekt Zeiger oder einen Speicher Zeiger von nachfolgenden Aufrufen an [**IMoniker:: bindesstorage**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtostorage) oder [**IMoniker:: bindtoken Object**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject)zurückzugeben, gibt der Moniker \_ an der \_ Stelle des Objekt Zeigers und NULL anstelle des Speicher Zeigers den Wert **null** zurück. Als Antwort muss der Client warten, bis das angeforderte Objekt oder der Speicher während der Implementierung von [**ibindstatus-Callback:: ondataavailable**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775061(v=vs.85)) und [**ibindstatus-Callback:: onobjectavailable**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775063(v=vs.85))empfangen wird.

Das Rückruf Objekt empfängt außerdem eine Status Benachrichtigung über [**IBindStatusCallback:: OnProgress**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775064(v=vs.85)), Daten Verfügbarkeits Benachrichtigung über [**ondataavailable**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775061(v=vs.85))und verschiedene andere Benachrichtigungen vom Moniker über den Status des Bindungs Vorgangs.

Wenn der Client nicht das \_ asynchrone bindf-Flag aus dem Aufruf von [**IBindStatusCallback:: getbindinfo**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775058(v=vs.85))des Monikers zurückgibt, wird der Bindungs Vorgang synchron fortgesetzt, und das gewünschte Objekt bzw. der gewünschte Speicher wird von nachfolgenden Aufrufen an [**BindTo Object**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject) oder [**BindTo Storage**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtostorage)zurückgegeben. Wenn der Client einen synchronen Vorgang wünscht und keine Status Benachrichtigungen oder-Rückrufe empfangen möchte, kann ein asynchroner Moniker so angefordert werden, dass er synchron verhält, indem er [**IBindStatusCallback**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775060(v=vs.85))nicht implementiert. In solchen Fällen verhält sich der asynchrone Moniker wie ein synchroner standardmoniker.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Asynchrone Moniker](asynchronous-monikers.md)
</dt> </dl>

 

 