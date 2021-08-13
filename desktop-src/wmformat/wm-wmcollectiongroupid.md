---
title: WM/WMCollectionGroupID
description: Das WM/WMCollectionGroupID-Attribut enthält eine GUID, die die Sammlungsgruppe identifiziert.
ms.assetid: 5cfa1747-ce3b-4e8d-bcce-84fb719123e8
keywords:
- WM/WMCollectionGroupID windows Media Format
topic_type:
- apiref
api_name:
- WM/WMCollectionGroupID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12b9d89724751e778eb9545b6c743dbfbcf077b860a8d85c5ab9297680deb930
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118698234"
---
# <a name="wmwmcollectiongroupid"></a>WM/WMCollectionGroupID

Das **WM/WMCollectionGroupID-Attribut** enthält eine GUID, die die Sammlungsgruppe identifiziert.

## <a name="global-constant"></a>Globale Konstante

g \_ wszWMWMCollectionGroupID

## <a name="data-type"></a>Datentyp

**\_ \_ WMT-TYP-GUID**

## <a name="remarks"></a>Hinweise

Inhalte werden von Windows Medientechnologien anhand von drei Werten identifiziert: **WM/WMCollectionGroupID**, **WM/WMCollectionID** und **WM/WMContentID**. Diese Werte identifizieren den Inhalt, die Auflistung, zu der sie gehört, und die Gruppe, zu der die Auflistung gehört. Alle drei Werte werden durch die Windows Media Player beim Abrufen von Metadaten für den Inhalt aufgefüllt. Sie können ihre Anwendung diese Werte aufzeichnen und verwenden, um Inhalte zu identifizieren. Sie sollten sie jedoch nicht ändern, wenn sie vorhanden sind.

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Attributliste**](attribute-list.md)
</dt> </dl>

 

 




