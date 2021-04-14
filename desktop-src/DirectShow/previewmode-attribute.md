---
description: Das PreviewMode-Attribut gibt den Vorschaumodus für die Gruppe an. Wenn der Wert true ist, können Frames während der Vorschau gelöscht werden. Andernfalls werden während der Vorschau keine Frames gelöscht. Der Standardwert ist TRUE.
ms.assetid: 5e4f4407-b43e-4b31-8676-1e12b6b70034
title: PreviewMode-Attribut
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d3b589b279a11b8ec329641ea2522a6a46dfa0e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104392601"
---
# <a name="previewmode-attribute"></a>PreviewMode-Attribut

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Das- `previewmode` Attribut gibt den Vorschaumodus für die Gruppe an. Wenn der Wert **true** ist, können Frames während der Vorschau gelöscht werden. Andernfalls werden während der Vorschau keine Frames gelöscht. Der Standardwert ist " **true**".

## <a name="possible-values"></a>Mögliche Werte

Die folgenden Werte sind als true definiert: y, y, t, t, 1. Die folgenden Werte sind als false definiert: n, n, f, f, 0 (null).

## <a name="applies-to"></a>Gilt für

[**Kreis**](group-element.md)

## <a name="remarks"></a>Bemerkungen

In der Standardeinstellung werden Frames beim Anzeigen der Vorschau von langsamen Effekten oder Übergängen gelöscht, damit das Video mit der Audiodatei synchronisiert wird. Das Video könnte als Ergebnis aussehen. Wenn dieses Attribut auf " **false** " festgelegt wird, wird jedes Frame während der Vorschau angezeigt, was dazu führen kann, dass das Video nicht mehr mit dem Audioformat synchronisiert wird Rahmen werden beim Schreiben in eine Datei nie gelöscht.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[XTL-Attribute](xtl-attributes.md)
</dt> <dt>

[**Iamtimelinegroup:: SetPreviewMode**](iamtimelinegroup-setpreviewmode.md)
</dt> </dl>

 

 



