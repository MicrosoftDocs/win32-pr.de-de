---
title: WM/WMContentID
description: Das WM/WMContentID-Attribut enthält eine GUID, die den Inhalt identifiziert.
ms.assetid: b46d02f4-04f5-430a-b3f7-0f80e03bed2c
keywords:
- WM/WMContentID-Windows-Medienformat
topic_type:
- apiref
api_name:
- WM/WMContentID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef6b1b77bf0305fa0890ea7e85172d77d6e213864c1fc114136bc42e08a8507b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119083864"
---
# <a name="wmwmcontentid"></a>WM/WMContentID

Das **WM/WMContentID-Attribut** enthält eine GUID, die den Inhalt identifiziert.

## <a name="global-constant"></a>Globale Konstante

g \_ wszWMWMContentID

## <a name="data-type"></a>Datentyp

**\_ \_ WMT-TYP-GUID**

## <a name="remarks"></a>Hinweise

Inhalte werden von Windows Medientechnologien anhand von drei Werten identifiziert: **WM/WMCollectionGroupID,** **WM/WMCollectionID** und **WM/WMContentID**. Diese Werte identifizieren den Inhalt, die Auflistung, zu der sie gehört, und die Gruppe, zu der die Auflistung gehört. Alle drei Werte werden durch die Windows Media Player beim Abrufen von Metadaten für den Inhalt aufgefüllt. Sie können ihre Anwendung diese Werte aufzeichnen und verwenden, um Inhalte zu identifizieren. Sie sollten sie jedoch nicht ändern, wenn sie vorhanden sind.

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Attributliste**](attribute-list.md)
</dt> </dl>

 

 




