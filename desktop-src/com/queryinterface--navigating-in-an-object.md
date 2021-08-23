---
title: QueryInterface-Navigation in einem Objekt
description: QueryInterface-Navigation in einem Objekt
ms.assetid: 7dec015f-7609-40eb-a71e-f6e9c9b9f8ff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdbb25f76f87b43f6fc4fc4d3a1a3eb65c19960942769818a83f176fc62f72c9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119611070"
---
# <a name="queryinterface-navigating-in-an-object"></a>QueryInterface: Navigieren in einem Objekt

Nachdem Sie über einen ersten Zeiger auf eine Schnittstelle eines Objekts verfügen, verfügt COM über einen sehr einfachen Mechanismus, um herauszufinden, ob das Objekt eine andere spezifische Schnittstelle unterstützt, und, falls ja, einen Zeiger darauf zu erhalten. (Informationen zum Abrufen eines ersten Zeigers auf eine Schnittstelle für ein Objekt finden Sie unter [Getting a Pointer to an Object](getting-a-pointer-to-an-object.md).) Dieser Mechanismus ist die [**QueryInterface-Methode**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) der [**IUnknown-Schnittstelle.**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) Wenn das -Objekt die angeforderte Schnittstelle unterstützt, muss die Methode einen Zeiger auf diese Schnittstelle zurückgeben. Dadurch kann ein Objekt frei durch die Schnittstellen navigieren, die ein Objekt unterstützt. **QueryInterface trennt** die Anforderung "Unterstützen Sie einen bestimmten Vertrag?" aus der hochleistungsbasierten Verwendung dieses Vertrags, sobald die Vertragserfüllung erfolgreich war.

Wenn ein Client anfänglich Zugriff auf ein Objekt erhält, erhält er mindestens einen [**IUnknown-Schnittstellenzeiger**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) (die grundlegendste Schnittstelle), über den er die Lebensdauer des Objekts steuern kann , indem er dem Objekt sagt, wann es mit dem -Objekt fertig ist, und [**QueryInterface aufrufen kann.**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) Der Client ist so programmiert, dass er jedes Objekt fragt, das er verwaltet, um einige Vorgänge auszuführen, aber die **IUnknown-Schnittstelle** verfügt über keine Funktionen für diese Vorgänge. Stattdessen werden diese Vorgänge über andere Schnittstellen ausgedrückt. Der Client ist daher so programmiert, dass er mit Objekten für diese Schnittstellen aushandelt. Insbesondere ruft der Client **QueryInterface** auf, um ein Objekt nach einer Schnittstelle zu fragen, über die der Client die gewünschten Vorgänge aufrufen kann.

Da das -Objekt [**QueryInterface implementiert,**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q))kann es die Anforderung annehmen oder ablehnen. Wenn das -Objekt die Clientanforderung akzeptiert, gibt **QueryInterface** einen neuen Zeiger auf die angeforderte Schnittstelle an den Client zurück. Über diesen Schnittstellenzeiger hat der Client Zugriff auf die Methoden dieser Schnittstelle. Wenn andererseits das -Objekt die Clientanforderung zurückgibt, gibt **QueryInterface** einen NULL-Zeiger zurück – einen Fehler – und der Client verfügt nicht über einen Zeiger, über den die gewünschten Funktionen aufruft werden können. In diesem Fall muss der Client diese Möglichkeit ordnungsgemäß behandeln. Angenommen, ein Client verfügt über einen Zeiger auf die Schnittstelle A für ein Objekt und fordert die Schnittstellen B und C an. Angenommen, das Objekt unterstützt auch Schnittstelle B, aber keine Schnittstelle C. Das Ergebnis ist, dass das -Objekt einen Zeiger auf B zurückgibt und meldet, dass C nicht unterstützt wird.

Ein wichtiger Punkt ist: Wenn ein Objekt einen Aufruf von [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q))ablehnt, kann der Client das Objekt nicht auffordern, die über die angeforderte Schnittstelle ausgedrückten Vorgänge auszuführen. Ein Client muss über einen Schnittstellenzeiger zum Aufrufen von Methoden in dieser Schnittstelle verfügen. Wenn das Objekt die Bereitstellung des angeforderten Zeigers verweigert, muss der Client darauf vorbereitet sein, darauf zu müssen, entweder nicht das zu tun, was er mit diesem Objekt beabsichtigt hatte, oder indem er versucht, auf eine andere, möglicherweise weniger leistungsfähige Schnittstelle zurückfallen zu müssen. Diese Funktion der COM-Funktionalität funktioniert gut im Vergleich zu anderen objektorientierten Systemen, in denen Sie nicht wissen können, ob eine Funktion funktioniert, bis Sie diese Funktion aufrufen, und selbst dann ist die Fehlerbehandlung unsicher. **QueryInterface bietet eine** zuverlässige und konsistente Möglichkeit zu wissen, ob ein Objekt eine Schnittstelle unterstützt, bevor versucht wird, seine Methoden auf aufruft.

Die [**QueryInterface-Methode**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) bietet auch eine stabile und zuverlässige Möglichkeit für ein Objekt, anzugeben, dass es keinen bestimmten Vertrag unterstützt. Das heißt, wenn in einem Aufruf von **QueryInterface** ein "altes" Objekt gefragt wird, ob es eine "neue" Schnittstelle unterstützt (z. B. eine Schnittstelle, die nach dem Versand des alten Objekts verunsichert war), antwortet das alte Objekt zuverlässig, ohne dass es zu einem Absturz führt, und antwortet "Nein". Die Technologie, die dies unterstützt, ist der Algorithmus, mit dem IIDs zugeordnet werden. Dies mag zwar wie ein kleiner Punkt erscheinen, aber es ist äußerst wichtig für die gesamte Architektur des Systems, und die Möglichkeit, ältere Elemente über neue Funktionen zu fragen, ist überraschenderweise ein Feature, das in den meisten anderen Objektarchitekturen nicht vorhanden ist.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden und Implementieren von IUnknown](using-and-implementing-iunknown.md)
</dt> </dl>

 

 




