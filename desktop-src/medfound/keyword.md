---
description: Gibt ein Schlüsselwort für einen MFTrace-Anbieter an.
ms.assetid: 1ce4a5ee-c053-4d31-a984-dc11acebbf2a
title: keyword-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9df1f7a648e7861dc8d248141f051e9911c9cb93257f47fee5f2b4d2fd9d5469
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119827550"
---
# <a name="keyword-element"></a>keyword-Element

Gibt ein Schlüsselwort für einen [MFTrace-Anbieter](mftrace.md) an.

## <a name="usage"></a>Verbrauch

``` syntax
<keyword
  ID = "CDATA"/>
```

## <a name="attributes"></a>Attribute



| attribute         | type             | Erforderlich       | BESCHREIBUNG                                             |
|-------------------|------------------|----------------|---------------------------------------------------------|
| **ID**<br/> | CDATA<br/> | Ja<br/> | Der Name oder die Maske des Schlüsselworts<br/> <br/> |



## <a name="child-elements"></a>Untergeordnete Elemente

Es gibt keine untergeordneten Elemente.

## <a name="parent-elements"></a>Übergeordnete Elemente

| Element                                   |
|-------------------------------------------|
| [**mfdetours**](mfdetours.md)<br/> |
| [**Anbieter**](provider.md)<br/>   |



## <a name="remarks"></a>Hinweise

Für das [**mfdetours-Element**](mfdetours.md) sind die gültigen Schlüsselwörter im Thema [MFTrace-Schlüsselwörter aufgeführt.](mftrace-keywords.md)

Für das [**Anbieterelement**](provider.md) hängen die Schlüsselwörter vom Ereignisanbieter ab. Sie können das Hilfsprogramm Wevtutil.exe verwenden, um die Schlüsselwörter für einen bestimmten Anbieter auflisten.

## <a name="element-information"></a>Elementinformationen

:::row:::
    :::column:::
        Kann leer bleiben
    :::column-end:::
    :::column span="2":::
        Ja
    :::column-end:::
:::row-end:::

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[MFTrace-Konfigurationsdatei](mftrace-configuration-file.md)
</dt> <dt>

[MFTrace-Schlüsselwörter](mftrace-keywords.md)
</dt> </dl>

 

 




