---
description: Gibt den Typ der Bestätigung an, der in einem icontextnode-Objekt auftreten kann.
ms.assetid: 5c906548-dbf5-4448-b248-070bd43b054e
title: ConfirmationType-Enumeration (iacom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConfirmationType
api_type:
- HeaderDef
api_location:
- IACom.h
ms.openlocfilehash: 2c43971c6ccf44513c11e46d4bc5db86d973d7f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345650"
---
# <a name="confirmationtype-enumeration"></a>ConfirmationType-Enumeration

Gibt den Typ der Bestätigung an, der in einem [**icontextnode**](icontextnode.md) -Objekt auftreten kann.

## <a name="syntax"></a>Syntax


```C++
typedef enum ConfirmationType { 
  ConfirmationType_None                   = 0,
  ConfirmationType_NodeTypeAndProperties  = 1,
  ConfirmationType_TopBoundary            = 4
} ConfirmationType;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="ConfirmationType_None"></span><span id="confirmationtype_none"></span><span id="CONFIRMATIONTYPE_NONE"></span>**ConfirmationType \_ None**
</dt> <dd>

Es wird keine Bestätigung angewendet. Der [**iinkanalyzer**](iinkanalyzer.md) kann einen Kontext Knoten oder einen seiner Nachfolger nach Bedarf ändern.

</dd> <dt>

<span id="ConfirmationType_NodeTypeAndProperties"></span><span id="confirmationtype_nodetypeandproperties"></span><span id="CONFIRMATIONTYPE_NODETYPEANDPROPERTIES"></span>**ConfirmationType \_ NodeTypeAndProperties**
</dt> <dd>

Der [**iinkanalyzer**](iinkanalyzer.md) kann den Typ oder keine Eigenschaften des angegebenen Kontext Knotens ändern.

</dd> <dt>

<span id="ConfirmationType_TopBoundary"></span><span id="confirmationtype_topboundary"></span><span id="CONFIRMATIONTYPE_TOPBOUNDARY"></span>**ConfirmationType- \_ TopBorder**
</dt> <dd>

Der [**iinkanalyzer**](iinkanalyzer.md) führt keine Vorgänge aus, z. b. das Hinzufügen von frei Hand Eingaben oder das Zusammenführen mit anderen [**ContextNodes**](icontextnodes.md), die bewirken, dass die topgrenze die aktuelle obere Grenze überschreitet. Beispiel:

-   Eine Anwendung analysiert eine Menge von frei Hand Eingaben, und es wird ein ParagraphNode identifiziert.
-   Die Anwendung bestätigt die topgrenze dieses Absatzes.
-   Der Benutzer der Anwendung schreibt neue frei Hand Eingaben oberhalb des aktuellen Absatzes. Wenn die Analyse erneut aufgerufen wird, wird die neue frei Hand Eingabe nicht in den bestätigten Absatz Knoten integriert.
-   Da nur die obere Grenze bestätigt wird, kann der ContextNode weiterhin in andere Richtungen vergrößert werden. Das Löschen von Strichen kann bewirken, dass die obere Grenze nach unten verschoben wird. Das Übersetzen von ContextNode kann dazu führen, dass sich der Speicherort ändert, aber keine weiteren frei Hand Eingaben an der neuen Position zusammengeführt werden.

Dieser ConfirmationType gilt nur für Absatz Knoten.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Sie können den **NoDebug typeandproperties** -Wert nur für frei Hand Wort-und frei Hand Zeichnungs Knoten verwenden (siehe [**icontextnode:: GetType**](icontextnode-gettype.md)). Andernfalls wird ein **E \_ invalidArg** von [**icontextnode:: Confirm**](icontextnode-confirm.md)zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]<br/>                                                 |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>Iacom. h (erfordert auch iacom \_ i. c)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Icontextnode:: Confirm**](icontextnode-confirm.md)
</dt> <dt>

[**Icontextnode:: isconfirmed**](icontextnode-isconfirmed.md)
</dt> </dl>

 

 




