---
title: QueryInterface-Navigation in einem Objekt
description: QueryInterface-Navigation in einem Objekt
ms.assetid: 7dec015f-7609-40eb-a71e-f6e9c9b9f8ff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3dbd44d200bf0a992f47bc375d0782bdadacf6a3
ms.sourcegitcommit: 85688bbfbe5b121bc05ddf112d54c23a469dfbc0
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "104314076"
---
# <a name="queryinterface-navigating-in-an-object"></a>QueryInterface: Navigieren in einem Objekt

Nachdem Sie einen anfänglichen Zeiger auf eine Schnittstelle für ein Objekt haben, verfügt com über einen sehr einfachen Mechanismus, um herauszufinden, ob das Objekt eine andere bestimmte Schnittstelle unterstützt, und wenn dies der Fall ist, um einen Zeiger darauf zu erhalten. (Informationen zum erhalten eines ersten Zeigers auf eine Schnittstelle für ein Objekt finden Sie unter " [erhalten eines Zeigers auf ein Objekt](getting-a-pointer-to-an-object.md)"). Dieser Mechanismus ist die [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) -Methode der [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) -Schnittstelle. Wenn das Objekt die angeforderte Schnittstelle unterstützt, muss die Methode einen Zeiger auf diese Schnittstelle zurückgeben. Dies ermöglicht es einem Objekt, durch die von einem Objekt unterstützten Schnittstellen frei zu navigieren. **QueryInterface** trennt die Anforderung "unterstützen Sie einen bestimmten Vertrag?" von der leistungsstarken Verwendung dieses Vertrags, wenn die Verhandlungen erfolgreich waren.

Wenn ein Client anfänglich auf ein Objekt zugreifen kann, empfängt der Client mindestens einen [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) -Schnittstellen Zeiger (die grundlegendste Schnittstelle), über den er die Lebensdauer des Objekts steuern kann – indem er das Objekt mit dem Objekt – teilt und [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q))aufruft. Der Client ist so programmiert, dass jedes Objekt, das es verwaltet, zum Ausführen einiger Vorgänge aufgefordert wird, aber die **IUnknown** -Schnittstelle verfügt über keine Funktionen für diese Vorgänge. Stattdessen werden diese Vorgänge über andere Schnittstellen ausgedrückt. Der Client ist daher so programmiert, dass er mit Objekten für diese Schnittstellen aushandelt. Insbesondere ruft der Client **QueryInterface** auf, um ein Objekt für eine Schnittstelle anzufordern, über die der Client die gewünschten Vorgänge aufrufen kann.

Da das-Objekt [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q))implementiert, ist es in der Lage, die Anforderung zu akzeptieren oder abzulehnen. Wenn das Objekt die Anforderung des Clients annimmt, gibt **QueryInterface** einen neuen Zeiger auf die angeforderte Schnittstelle an den Client zurück. Über diesen Schnittstellen Zeiger hat der Client Zugriff auf die Methoden dieser Schnittstelle. Wenn hingegen das Objekt die Anforderung des Clients zurückweist, gibt **QueryInterface** einen NULL-Zeiger zurück – einen Fehler –, und der Client hat keinen Zeiger, über den die gewünschten Funktionen aufgerufen werden. In diesem Fall muss der Client diese Möglichkeit ordnungsgemäß behandeln. Angenommen, ein Client verfügt über einen Zeiger auf die Schnittstelle a für ein Objekt und fordert die Schnittstellen b und C an. nehmen Sie auch an, dass das Objekt Schnittstelle b unterstützt, aber Schnittstelle C nicht unterstützt. Das Ergebnis ist, dass das-Objekt einen Zeiger auf B zurückgibt und meldet, dass C nicht unterstützt wird.

Ein wichtiger Punkt ist, dass der Client das Objekt nicht zum Ausführen der Vorgänge auffordern kann, die über die angeforderte Schnittstelle ausgedrückt werden, wenn ein Objekt einen aufzurufenden [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q))-Rückruf ablehnt. Ein Client muss über einen Schnittstellen Zeiger verfügen, um Methoden in dieser Schnittstelle aufzurufen. Wenn das Objekt den angeforderten Zeiger nicht bereitstellen möchte, muss der Client für die Verwendung von vorbereitet sein, und zwar entweder durch das Ausführen eines anderen, was mit diesem Objekt beabsichtigt war, oder durch einen Versuch, auf eine andere, vielleicht weniger leistungsfähige Schnittstelle zurückzukommen. Diese Funktion der com-Funktionalität eignet sich gut für andere objektorientierte Systeme, bei denen Sie nicht wissen, ob eine Funktion funktioniert, bis Sie diese Funktion aufgerufen haben. selbst dann ist die Behandlung von Fehlern unsicher. **QueryInterface** bietet eine zuverlässige und konsistente Möglichkeit zu wissen, ob ein Objekt eine Schnittstelle unterstützt, bevor versucht wird, seine Methoden aufzurufen.

Die [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) -Methode bietet auch einen robusten und zuverlässigen Weg für ein Objekt, um anzugeben, dass ein bestimmter Vertrag nicht unterstützt wird. Das heißt, wenn in einem Anruf von **QueryInterface** One ein "altes" Objekt anfordert, ob es eine "neue" Schnittstelle unterstützt (z. b., die nach dem Versenden des alten Objekts erfunden wurde), wird das alte Objekt zuverlässig, ohne einen Absturz zu verursachen, mit "Nein" beantwortet. Die Technologie, die dies unterstützt, ist der Algorithmus, mit dem IIDs zugewiesen werden. Dies mag ein kleiner Punkt sein, aber es ist äußerst wichtig für die allgemeine Architektur des Systems, und die Fähigkeit, Legacy Elemente zu neuen Funktionen zu befragen, ist überraschend ein Feature, das in den meisten anderen Objekt Architekturen nicht vorhanden ist.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden und Implementieren von IUnknown](using-and-implementing-iunknown.md)
</dt> </dl>

 

 




