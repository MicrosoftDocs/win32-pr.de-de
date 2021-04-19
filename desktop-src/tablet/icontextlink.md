---
description: Stellt eine Beziehung zwischen zwei icontextnode-Objekten dar.
ms.assetid: ee81d9d7-eba9-4b11-84d0-5a6ca0df7d92
title: Icontextlink-Schnittstelle (iacom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextLink
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: df1e0d8717ba29532486277aced19f17adb1d79c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106357353"
---
# <a name="icontextlink-interface"></a>Icontextlink-Schnittstelle

Stellt eine Beziehung zwischen zwei [**icontextnode**](icontextnode.md) -Objekten dar.

## <a name="members"></a>Member

Die **icontextlink** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **Icontextlink** enthält auch die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **icontextlink** -Schnittstelle verfügt über diese Methoden.



| Methode                                                                  | BESCHREIBUNG                                                                                                             |
|:------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------|
| [**Getcontextlinkdirection**](icontextlink-getcontextlinkdirection.md) | Ruft den Beziehungstyp ab, den dieser **icontextlink** darstellt.<br/>                                         |
| [**Getdestinationnode**](icontextlink-getdestinationnode.md)           | Ruft das [**icontextnode**](icontextnode.md) -Objekt ab, das das Ziel für diesen **icontextlink** ist.<br/> |
| [**Getsourcenode**](icontextlink-getsourcenode.md)                     | Ruft das [**icontextnode**](icontextnode.md) -Objekt ab, das die Quelle für diesen **icontextlink** ist.<br/>      |



 

## <a name="remarks"></a>Bemerkungen

Im folgenden finden Sie ein Beispiel für eine Beziehung, die durch ein **icontextlink** -Objekt dargestellt wird:

-   Wenn ein AnalysisHint-Knoten in der Handschrift Analyse verwendet wird, erstellt der Ink-Analyse Vorgang ein **icontextlink** -Objekt vom Typ AnalysisHint zwischen dem Knoten des Analyse Hinweises und dem Knoten, der das Schreiben innerhalb des Bereichs des Hinweises enthält. Der Quellknoten ist der Analyse Hinweis Knoten, und der Zielknoten ist der Knoten, der Schreibvorgänge enthält.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]<br/>                                                 |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>Iacom. h (erfordert auch iacom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Icontextnode:: getcontextlinks**](icontextnode-getcontextlinks.md)
</dt> <dt>

[**Icontextlinks**](icontextlinks.md)
</dt> <dt>

[**ContextLinkDirection**](contextlinkdirection.md)
</dt> <dt>

[Kontext Knoten Typen](context-node-types.md)
</dt> </dl>

 

