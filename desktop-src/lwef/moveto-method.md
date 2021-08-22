---
title: MoveTo-Methode
description: MoveTo-Methode
ms.assetid: cca2b1b8-0d44-4272-9f0b-f7afd091d802
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58a245d389bc23d79d9f6cc105fec28ed14f5d511123c1dd113115ff69fc95c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119609080"
---
# <a name="moveto-method"></a>MoveTo-Methode

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**
</dt> <dd>

Verschiebt das angegebene Zeichen an die angegebene Position.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

*agent***. Zeichen ("**_CharacterID_*_"). MoveTo_ *  *x,y* \[ *Speed*\]



| Teil    | Beschreibung                                                                                                                                                                                     |
|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *x,y*   | Erforderlich. Ein ganzzahliger Wert, der den linken Rand (*x*) und den oberen Rand (*y*) des Animationsframes angibt. Diese Koordinaten werden in Pixel ausgedrückt.                                                   |
| *Geschwindigkeit* | Optional. Ein ganzzahliger Wert vom Typ Long, der in Millisekunden angibt, wie schnell sich der Rahmen des Zeichens bewegt. Der Standardwert lautet „1000“. Wenn Null (0) angegeben wird, wird der Frame ohne Wiedergabe einer Animation verschoben. |



 

</dd> </dl>

## <a name="remarks"></a>Hinweise

Der Server gibt automatisch die entsprechende Animation wieder, die den **Bewegungszuständen** zugewiesen ist. Die Position eines Zeichens basiert auf der oberen linken Ecke des Rahmens.

Wenn Sie eine Objektvariable deklarieren und auf diese Methode festlegen, wird ein [**Request-Objekt**](/windows/desktop/lwef/the-request-object) zurückgegeben. Wenn die zugeordnete Animation nicht auf dem lokalen Computer geladen wurde, legt der Server außerdem die [**Status-Eigenschaft**](status-property.md) des **Request-Objekts** auf "Failed" mit einer entsprechenden Fehlernummer fest. Wenn Sie das HTTP-Protokoll verwenden, um auf Zeichen- oder Animationsdaten zuzugreifen, verwenden [**Sie**](get-method.md) daher die Get-Methode, um die **Animationen** des Moving-Zustands zu laden, bevor Sie die **MoveTo-Methode** aufrufen.

Auch wenn die Animation nicht geladen ist, verschiebt der Server den Frame trotzdem.

> [!Note]  
> Wenn Sie **MoveTo** mit einem Wert ungleich 0 (null) aufrufen, bevor das Zeichen angezeigt wird, wird ein Fehlerstatus zurückgegeben, wenn Sie ihm ein [**Request-Objekt**](/windows/desktop/lwef/the-request-object) zugewiesen haben, da der Wert ungleich 0 (null) angibt, dass Sie versuchen, eine Animation wiederzuspielen, wenn das Zeichen nicht sichtbar ist.

 

> [!Note]  
> Der tatsächliche Effekt des *Speed-Parameters* kann abhängig von der Geschwindigkeit des Prozessors des Computers und der Priorität anderer Aufgaben variieren, die auf dem System ausgeführt werden.

 

 

 