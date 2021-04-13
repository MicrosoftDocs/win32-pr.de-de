---
title: WM/wmcontentid
description: Das WM/wmcontentid-Attribut enthält eine GUID, die den Inhalt identifiziert.
ms.assetid: b46d02f4-04f5-430a-b3f7-0f80e03bed2c
keywords:
- WM/wmcontentid Windows Media-Format
topic_type:
- apiref
api_name:
- WM/WMContentID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56ef250e2e2e797ce5ba3c4492c2a3f8b71d30eb
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104389212"
---
# <a name="wmwmcontentid"></a>WM/wmcontentid

Das **WM/wmcontentid-** Attribut enthält eine GUID, die den Inhalt identifiziert.

## <a name="global-constant"></a>Globale Konstante

g \_ wszwmwmcontentid

## <a name="data-type"></a>Datentyp

**WMT- \_ Typ- \_ GUID**

## <a name="remarks"></a>Bemerkungen

Der Inhalt wird von Windows Media-Technologien mithilfe von drei Werten identifiziert: **WM/wmcollectiongroupid**, **WM/wmcollectionid** und **WM/wmcontentid**. Mit diesen Werten werden der Inhalt, die Auflistung, zu der er gehört, und die Gruppe, zu der die Auflistung gehört, identifiziert. Alle drei Werte werden von Windows Media Player aufgefüllt, wenn Metadaten für den Inhalt abgerufen werden. Sie können festlegen, dass Ihre Anwendung diese Werte aufzeichnen und Sie verwenden, um Inhalte zu identifizieren, Sie sollten Sie jedoch nicht ändern, wenn Sie vorhanden sind.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Attributliste**](attribute-list.md)
</dt> </dl>

 

 




