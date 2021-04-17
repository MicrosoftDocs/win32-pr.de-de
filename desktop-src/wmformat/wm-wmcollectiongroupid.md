---
title: WM/wmcollectiongroupid
description: Das WM/wmcollectiongroupid-Attribut enthält eine GUID, die die Sammlungs Gruppe identifiziert.
ms.assetid: 5cfa1747-ce3b-4e8d-bcce-84fb719123e8
keywords:
- WM/wmcollectiongroupid Windows Media-Format
topic_type:
- apiref
api_name:
- WM/WMCollectionGroupID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 652007933669db4ed7977474858c7089ca0d577f
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104389213"
---
# <a name="wmwmcollectiongroupid"></a>WM/wmcollectiongroupid

Das **WM/wmcollectiongroupid-** Attribut enthält eine GUID, die die Sammlungs Gruppe identifiziert.

## <a name="global-constant"></a>Globale Konstante

g \_ wszwmwmcollectiongroupid

## <a name="data-type"></a>Datentyp

**WMT- \_ Typ- \_ GUID**

## <a name="remarks"></a>Bemerkungen

Der Inhalt wird von Windows Media-Technologien mithilfe von drei Werten identifiziert: **WM/wmcollectiongroupid**, **WM/wmcollectionid** und **WM/wmcontentid**. Mit diesen Werten werden der Inhalt, die Auflistung, zu der er gehört, und die Gruppe, zu der die Auflistung gehört, identifiziert. Alle drei Werte werden von Windows Media Player aufgefüllt, wenn Metadaten für den Inhalt abgerufen werden. Sie können festlegen, dass Ihre Anwendung diese Werte aufzeichnen und Sie verwenden, um Inhalte zu identifizieren, Sie sollten Sie jedoch nicht ändern, wenn Sie vorhanden sind.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Attributliste**](attribute-list.md)
</dt> </dl>

 

 




