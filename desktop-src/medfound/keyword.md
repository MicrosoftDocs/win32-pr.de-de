---
description: Gibt ein Schlüsselwort für einen MFTrace-Anbieter an.
ms.assetid: 1ce4a5ee-c053-4d31-a984-dc11acebbf2a
title: Schlüsselwortelement
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ba871fea760ed3b604048ade2722afc0323e03b
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119375"
---
# <a name="keyword-element"></a>Schlüsselwortelement

Gibt ein Schlüsselwort für einen [MFTrace-Anbieter](mftrace.md) an.

## <a name="usage"></a>Verwendung

``` syntax
<keyword
  ID = "CDATA"/>
```

## <a name="attributes"></a>Attribute



| attribute         | Typ             | Erforderlich       | BESCHREIBUNG                                             |
|-------------------|------------------|----------------|---------------------------------------------------------|
| **ID**<br/> | CDATA<br/> | Ja<br/> | Name oder Maske des Schlüsselworts<br/> <br/> |



## <a name="child-elements"></a>Untergeordnete Elemente

Es gibt keine untergeordneten Elemente.

## <a name="parent-elements"></a>Übergeordnete Elemente

| Element                                   |
|-------------------------------------------|
| [**mfdetours**](mfdetours.md)<br/> |
| [**Anbieter**](provider.md)<br/>   |



## <a name="remarks"></a>Bemerkungen

Für das [**mfdetours-Element**](mfdetours.md) sind die gültigen Schlüsselwörter im Thema [MFTrace Keywords](mftrace-keywords.md)aufgeführt.

Für das [**Anbieterelement**](provider.md) hängen die Schlüsselwörter vom Ereignisanbieter ab. Sie können das hilfsprogramm Wevtutil.exe verwenden, um die Schlüsselwörter für einen bestimmten Anbieter aufzulisten.

## <a name="element-information"></a>Elementinformationen

:::row:::
    :::column:::
        Kann leer bleiben
    :::column-end:::
    :::column span="2":::
        Ja
    :::column-end:::
:::row-end:::

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[MFTrace-Konfigurationsdatei](mftrace-configuration-file.md)
</dt> <dt>

[MFTrace-Schlüsselwörter](mftrace-keywords.md)
</dt> </dl>

 

 




