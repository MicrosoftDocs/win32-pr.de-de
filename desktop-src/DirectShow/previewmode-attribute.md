---
description: Das previewmode-Attribut gibt den Vorschaumodus für die Gruppe an. Wenn der Wert TRUE ist, können Frames während der Vorschau gelöscht werden. Andernfalls werden während der Vorschau keine Frames gelöscht. Der Standardwert ist TRUE.
ms.assetid: 5e4f4407-b43e-4b31-8676-1e12b6b70034
title: previewmode-Attribut
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6baed13417539432a3a2958b96b214c3c63ae12f2802586ca220669b1497d91f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119748270"
---
# <a name="previewmode-attribute"></a>previewmode-Attribut

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Releases von Windows entfernt werden.\]

 

Das `previewmode` -Attribut gibt den Vorschaumodus für die Gruppe an. Wenn der Wert **TRUE** ist, können Frames während der Vorschau gelöscht werden. Andernfalls werden während der Vorschau keine Frames gelöscht. Der Standardwert ist **TRUE.**

## <a name="possible-values"></a>Mögliche Werte

Die folgenden Werte sind als TRUE definiert: y, Y, t, T, 1. Die folgenden Werte sind als FALSE definiert: n, N, f, F, 0 (null).

## <a name="applies-to"></a>Gilt für

[**group**](group-element.md)

## <a name="remarks"></a>Hinweise

Unter der Standardeinstellung werden Frames während der Vorschau von langsamen Effekten oder Übergängen gelöscht, um das Video mit dem Audio synchronisiert zu halten. Das Video könnte als Ergebnis geschnitten aussehen. Das Festlegen dieses Attributs auf **FALSE** erzwingt, dass jeder Frame während der Vorschau gerendert wird, was möglicherweise dazu führt, dass das Video nicht mehr mit dem Audio synchronisiert wird. Frames werden beim Schreiben in eine Datei nie gelöscht.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[XTL-Attribute](xtl-attributes.md)
</dt> <dt>

[**IAMTimelineGroup::SetPreviewMode**](iamtimelinegroup-setpreviewmode.md)
</dt> </dl>

 

 



