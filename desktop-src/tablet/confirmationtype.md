---
description: Gibt den Bestätigungstyp an, der für ein IContextNode-Objekt auftreten kann.
ms.assetid: 5c906548-dbf5-4448-b248-070bd43b054e
title: ConfirmationType-Enumeration (IACom.h)
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
ms.openlocfilehash: 9f89d5457e3d75bcf781a100449e4da9f8b45624af38760ca0cdda358fbf47ea
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119936950"
---
# <a name="confirmationtype-enumeration"></a>ConfirmationType-Enumeration

Gibt den Bestätigungstyp an, der für ein [**IContextNode-Objekt**](icontextnode.md) auftreten kann.

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

Es wird keine Bestätigung angewendet. [**IInkAnalyzer**](iinkanalyzer.md) kann einen Kontextknoten oder eines seiner Nachfolger nach Bedarf ändern.

</dd> <dt>

<span id="ConfirmationType_NodeTypeAndProperties"></span><span id="confirmationtype_nodetypeandproperties"></span><span id="CONFIRMATIONTYPE_NODETYPEANDPROPERTIES"></span>**ConfirmationType \_ NodeTypeAndProperties**
</dt> <dd>

Der [**IInkAnalyzer**](iinkanalyzer.md) kann den Typ oder eigenschaften des angegebenen Kontextknotens nicht ändern.

</dd> <dt>

<span id="ConfirmationType_TopBoundary"></span><span id="confirmationtype_topboundary"></span><span id="CONFIRMATIONTYPE_TOPBOUNDARY"></span>**ConfirmationType \_ TopBoundary**
</dt> <dd>

[**IInkAnalyzer**](iinkanalyzer.md) führt keine Vorgänge aus, z. B. das Hinzufügen von Freihand oder das Zusammenführen mit anderen [**ContextNodes,**](icontextnodes.md)die dazu führen, dass TopBoundary die aktuelle obere Grenze übersteigt. Beispiel:

-   Eine Anwendung analysiert einen Satz Von Ink, und ein ParagraphNode wird identifiziert.
-   Die Anwendung bestätigt den TopBoundary dieses Absatzes.
-   Der Benutzer der Anwendung schreibt neue Ink über dem aktuellen Absatz. Wenn analyze erneut aufgerufen wird, wird die neue Ink nicht in den Knoten Bestätigter Absatz integriert.
-   Da nur die obere Grenze bestätigt wird, kann der ContextNode in andere Richtungen weiter wachsen. Das Löschen von Strichen kann dazu führen, dass die obere Grenze nach unten verschoben wird. Die Übersetzung des ContextNode kann dazu führen, dass sich der Speicherort ändert, aber es wird nicht zugelassen, dass zusätzliche Ink-Dateien am neuen Speicherort zusammengeführt werden.

Dieser ConfirmationType gilt nur für Absatzknoten.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Sie können den **NodeTypeAndProperties-Wert** nur für Freihandwort- und Freihandzeichnungsknoten verwenden (siehe [**IContextNode::GetType**](icontextnode-gettype.md)). Andernfalls wird eine **E \_ INVALIDARG** von [**IContextNode::Confirm**](icontextnode-confirm.md)zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur Desktop-Apps der XP Tablet PC Edition \[\]<br/>                                                 |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>IACom.h (erfordert auch IACom \_ i.c)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IContextNode::Confirm**](icontextnode-confirm.md)
</dt> <dt>

[**IContextNode::IsConfirmed**](icontextnode-isconfirmed.md)
</dt> </dl>

 

 




