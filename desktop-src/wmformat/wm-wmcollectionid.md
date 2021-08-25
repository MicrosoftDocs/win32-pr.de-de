---
title: WM/WMCollectionID
description: Das WM/WMCollectionID-Attribut enthält eine GUID, die die Sammlung identifiziert.
ms.assetid: 088fe2d7-e2d9-42a3-8deb-1d7948ff7df9
keywords:
- WM/WMCollectionID windows Media Format
topic_type:
- apiref
api_name:
- WM/WMCollectionID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9ad7e22c6769d459dc3d99b964a2df8e4dc562c709a231163d05a1b6b0be911
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119928830"
---
# <a name="wmwmcollectionid"></a>WM/WMCollectionID

Das **WM/WMCollectionID-Attribut** enthält eine GUID, die die Sammlung identifiziert.

## <a name="global-constant"></a>Globale Konstante

g \_ wszWMWMCollectionID

## <a name="data-type"></a>Datentyp

**\_ \_ WMT-TYP-GUID**

## <a name="remarks"></a>Hinweise

Inhalte werden von Windows Medientechnologien anhand von drei Werten identifiziert: **WM/WMCollectionGroupID,** **WM/WMCollectionID** und **WM/WMContentID**. Diese Werte identifizieren den Inhalt, die Auflistung, zu der sie gehört, und die Gruppe, zu der die Auflistung gehört. Alle drei Werte werden durch die Windows Media Player beim Abrufen von Metadaten für den Inhalt aufgefüllt. Sie können ihre Anwendung diese Werte aufzeichnen und verwenden, um Inhalte zu identifizieren. Sie sollten sie jedoch nicht ändern, wenn sie vorhanden sind.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Attributliste**](attribute-list.md)
</dt> </dl>

 

 




