---
title: Show-Methode
description: Show-Methode
ms.assetid: 58adbb55-f4cb-4356-abc4-b85fa3af744d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ede9dd8474b21911fccb0c217b070dbfb84160125d2fd56092685ccaf82905b2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118475352"
---
# <a name="show-method"></a>Show-Methode

\[Microsoft Agent ist ab Version Windows 7 veraltet und in nachfolgenden Versionen von Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**
</dt> <dd>

Macht das angegebene Zeichen sichtbar und gibt die zugeordnete **Anzeigeanimation** wieder.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

*agent***. Zeichen ("**_CharacterID_*_"). Schnell_ *  \[ *anzeigen*\]



| Teil   | BESCHREIBUNG                                                                                                                                                                                                                              |
|--------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *Fast* | Optional. Ein boolescher Ausdruck, der an gibt, ob der Server die **Showing-Animation wieder** spielt. **True** Überspringt die **Animation Zum** Anzeigen des Zustands. <br/> **False** (Standard) Überspringt die Animation **Zum Anzeigen des** Zustands nicht. <br/> |



 

</dd> </dl>

## <a name="remarks"></a>Hinweise

Wenn Sie einen Objektverweis deklarieren und auf diese Methode festlegen, wird ein [**Request-Objekt**](/windows/desktop/lwef/the-request-object) zurückgegeben. Wenn die zugeordnete  Showing-Animation nicht geladen wurde und Sie den **Fast-Parameter** nicht  als **True** angegeben haben, legt der Server die [**Status-Eigenschaft**](status-property.md) des Anforderungsobjekts mit einer entsprechenden Fehlernummer auf "failed" fest. Wenn Sie daher das HTTP-Protokoll für den Zugriff auf Zeichenanimationsdaten verwenden, verwenden Sie die [**Get-Methode,**](get-method.md) um die Animation zum Anzeigen des Zustands zu laden, bevor Sie die **Show-Methode** aufrufen. 

Vermeiden Sie es, den **Fast-Parameter** auf **TRUE zu** setzen, ohne zuvor eine Animation wiedergibt. Andernfalls wird der Zeichenrahmen möglicherweise ohne Bild angezeigt. Beachten Sie insbesondere Folgendes: Wenn Sie [**MoveTo**](moveto-method.md) aufrufen, wenn das Zeichen nicht sichtbar ist, wird keine Animation wieder verwendet. Wenn Sie daher die Show-Methode **aufrufen,** bei **der Fast** auf True festgelegt **ist,** wird kein Bild angezeigt. Wenn Sie Ausblenden und dann  [**Schnell**](hide-method.md) anzeigen auf  **True** festlegen, wird kein Bild angezeigt.

## <a name="see-also"></a>Weitere Informationen

[**Hide-Methode**](hide-method.md)


 

