---
title: WM/wmcollectionid
description: Das WM/wmcollectionid-Attribut enthält eine GUID, die die Auflistung identifiziert.
ms.assetid: 088fe2d7-e2d9-42a3-8deb-1d7948ff7df9
keywords:
- WM/wmcollectionid Windows Media-Format
topic_type:
- apiref
api_name:
- WM/WMCollectionID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21d2ffe9ca827b19b4ce403b2e2929dea64ae684
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104389214"
---
# <a name="wmwmcollectionid"></a>WM/wmcollectionid

Das **WM/wmcollectionid-** Attribut enthält eine GUID, die die Auflistung identifiziert.

## <a name="global-constant"></a>Globale Konstante

g \_ wszwmwmcollectionid

## <a name="data-type"></a>Datentyp

**WMT- \_ Typ- \_ GUID**

## <a name="remarks"></a>Bemerkungen

Der Inhalt wird von Windows Media-Technologien mithilfe von drei Werten identifiziert: **WM/wmcollectiongroupid**, **WM/wmcollectionid** und **WM/wmcontentid**. Mit diesen Werten werden der Inhalt, die Auflistung, zu der er gehört, und die Gruppe, zu der die Auflistung gehört, identifiziert. Alle drei Werte werden von Windows Media Player aufgefüllt, wenn Metadaten für den Inhalt abgerufen werden. Sie können festlegen, dass Ihre Anwendung diese Werte aufzeichnen und Sie verwenden, um Inhalte zu identifizieren, Sie sollten Sie jedoch nicht ändern, wenn Sie vorhanden sind.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Attributliste**](attribute-list.md)
</dt> </dl>

 

 




