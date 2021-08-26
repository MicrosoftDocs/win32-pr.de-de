---
title: Implementieren und Aktivieren eines Handlers mit zusätzlichen vom Server bereitgestellten Daten
description: Implementieren und Aktivieren eines Handlers mit zusätzlichen vom Server bereitgestellten Daten
ms.assetid: 5bbf81bd-430d-4008-b1cc-9ea91bb3b1e7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4777c44dd9983a0193872507272862766c51e708f5caa491a6f8d787923749c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120029928"
---
# <a name="implementing-and-activating-a-handler-with-extra-data-supplied-by-server"></a>Implementieren und Aktivieren eines Handlers mit zusätzlichen vom Server bereitgestellten Daten

Wenn der Server zusätzliche Daten in das Paket integrieren möchte, damit der Handler verwendet werden kann, muss der Server sowohl die [**IMarshal-**](/windows/win32/api/objidlbase/nn-objidlbase-imarshal) als auch die [**IStdMarshalInfo-Schnittstelle**](/windows/win32/api/objidlbase/nn-objidlbase-istdmarshalinfo) implementieren. Der Server muss den Standardmarshaller aggregieren und den ersten Teil des Marshallings an den aggregierten Standardmaraler delegieren, einschließlich [**IMarshal::GetUnmarshalClass,**](/windows/desktop/api/ObjIdl/nf-objidl-imarshal-getunmarshalclass)und der Größe, die vom [**IMarshal::GetMarshalSizeMax**](/windows/desktop/api/ObjIdl/nf-objidl-imarshal-getmarshalsizemax)des Standardmaralers zurückgegeben wird, eine eigene Datengröße hinzufügen. Der Standardmarshaller ruft [**IStdMarshalInfo::GetClassForHandler**](/windows/win32/api/objidlbase/nf-objidlbase-istdmarshalinfo-getclassforhandler) auf, um die CLSID des zu erstellenden Handlers zu erhalten. Nachdem der Standard-Marshaller das Marshalling durchgeführt hat, schreibt der Server seine eigenen zusätzlichen Daten in den Stream. Die resultierenden Strukturen mit zusätzlichen Daten im Stream sind in der folgenden Abbildung dargestellt:

![Diagramm, das Strukturen mit zusätzlichen Daten im Stream zeigt.](images/4cff306b-bb82-4c05-8e64-7ca73731f265.png)

## <a name="server-side-structures-with-extra-data-in-stream"></a>Server-Side Strukturen mit zusätzlichen Daten in Stream

Dies ermöglicht dem Aufruf von COM an [**CoUnmarshalInterface**](/windows/desktop/api/combaseapi/nf-combaseapi-counmarshalinterface) auf Clientseite die Möglichkeit, ungelesene Daten zu überspringen und den Stream an der entsprechenden Position hinter allen gemarshallten Schnittstellendaten zu belassen, wenn der Handler nicht erstellt werden kann.

## <a name="client-side-structures-with-extra-data-in-stream"></a>Client-Side Strukturen mit zusätzlichen Daten in Stream

Wie im Fall, dass keine zusätzlichen Serverdaten im Stream gespeichert sind, erstellt der clientseitige COM-Aufruf von [**CoUnmarshalInterface**](/windows/desktop/api/combaseapi/nf-combaseapi-counmarshalinterface) die Identität und den Handler. Der Handler muss [**IMarshal**](/windows/win32/api/objidlbase/nn-objidlbase-imarshal) implementieren und die **IMarshal-Aufrufe** zuerst an den aggregierten Standardmarshaller delegieren und dann alle zusätzlichen Daten marshallen oder entmarshalieren, die der Server bereitgestellt hat. Das [**UnmarshalInterface**](/windows/win32/api/objidlbase/nf-objidlbase-imarshal-unmarshalinterface) des Handlers wird für jedes Nichtmarshal aufgerufen, unabhängig davon, ob die Schnittstelle zuvor entmarshalt wurde oder nicht. In diesem Fall wird [**coGetStdMarshalEx**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetstdmarshalex) vom Server nicht aufgerufen, der Handler muss es jedoch. Die resultierende clientseitige Struktur wird in der folgenden Abbildung dargestellt.

![Diagramm, das die clientseitige Struktur zeigt.](images/053411c7-9d54-4ae5-bcb6-778454b1d86f.png)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Der LightweightClient-Side Handler](the-lightweight-client-side-handler.md)
</dt> </dl>

 

 