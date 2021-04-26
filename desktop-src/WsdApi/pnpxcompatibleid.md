---
description: Gibt den PnP-X-kompatiblen Bezeichner des Diensts an. Geräte können über mehrere kompatible IDs verfügen.
ms.assetid: 25f3d06e-460c-4338-b05d-a6d2c10c2a12
title: PnPXCompatibleId-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f4a02191e2186926e5f26e5609aec82ff87f851f
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996637"
---
# <a name="pnpxcompatibleid-element"></a>PnPXCompatibleId-Element

Gibt den PnP-X-kompatiblen Bezeichner des Diensts an. Geräte können über mehrere kompatible IDs verfügen.

## <a name="usage"></a>Verbrauch

``` syntax
<PnPXCompatibleId/>
```

## <a name="attributes"></a>Attribute

Es gibt keine Attribute.

## <a name="child-elements"></a>Untergeordnete Elemente

Es gibt keine untergeordneten Elemente.

## <a name="parent-elements"></a>Übergeordnete Elemente



| Element                             | BESCHREIBUNG                                                                            |
|-------------------------------------|----------------------------------------------------------------------------------------|
| [**Gehostet**](hosted.md)<br/> | Definiert Elemente für die vom Diensthost definierten Dienste. <br/> <br/> |



## <a name="remarks"></a>Hinweise

Um mehr als eine CompatibleID anzugeben, trennen Sie die Bezeichner durch ein Leerzeichen, z.B. "PnPX \_ SampleService \_ HWID \_ 1 PnPX \_ SampleService \_ HWID \_ 2 PnPX \_ SampleService1 \_ HWID \_ 3".

## <a name="element-information"></a>Elementinformationen



| Bezeichnung | Wert |
|-------------------------------------|---------------|
| Unterstützte Mindestversion (System)<br/> | Windows Vista |
| Kann leer bleiben                        | Ja           |



 

 




