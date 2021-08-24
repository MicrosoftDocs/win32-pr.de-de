---
title: GestureAt-Methode
description: GestureAt-Methode
ms.assetid: c84e9363-e905-476a-832b-9acf6ddee5f1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d7c18c2a3913e8c9e805725f184bd5e969de6272ed05c562799805bd8c74256
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119725720"
---
# <a name="gestureat-method"></a>GestureAt-Methode

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**
</dt> <dd>

Gibt die Gesturinganimation für das angegebene Zeichen an der angegebenen Position wieder.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

*agent***. Zeichen ("**_CharacterID_*_"). GestureAt_ *  *x,y*



| Teil  | Beschreibung                                                                                                                                                                                               |
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *x,y* | Erforderlich. Ein ganzzahliger Wert, der die horizontale Bildschirmkoordinate (*x*) und die vertikale Bildschirmkoordinate (*y*) angibt, auf die das Zeichen zeigt. Diese Koordinaten müssen in Pixel angegeben werden. |



 

</dd> </dl>

## <a name="remarks"></a>Hinweise

Der Server gibt automatisch die entsprechende Animation ab, um eine Geste an die angegebene Position zu bewegen. Die Koordinaten sind immer relativ zum Bildschirmursprung (oben links).

Wenn Sie einen Objektverweis deklarieren und auf diese Methode festlegen, wird ein [**Request-Objekt**](/windows/desktop/lwef/the-request-object) zurückgegeben. Wenn die zugeordnete Animation nicht auf dem lokalen Computer geladen wurde, legt der Server außerdem die [**Status-Eigenschaft**](status-property.md) des **Request-Objekts** auf "failed" mit einer entsprechenden Fehlernummer fest. Wenn Sie das HTTP-Protokoll für den Zugriff auf Zeichenanimationsdaten verwenden, verwenden [**Sie**](get-method.md) daher die Get-Methode, um die Gesturing-Zustandsanimationen zu laden, bevor Sie die **GestureAt-Methode** aufrufen. 

 

 