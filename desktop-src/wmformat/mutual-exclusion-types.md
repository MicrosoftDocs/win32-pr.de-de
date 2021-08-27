---
title: Gegenseitige Ausschlusstypen
description: Gegenseitige Ausschlusstypen
ms.assetid: bfe6cfe6-3df4-49c4-8015-fe4479b693c1
keywords:
- Windows Medienformat-SDK, gegenseitiger Ausschluss
- Advanced Systems Format (ASF), gegenseitiger Ausschluss
- ASF (Advanced Systems Format), gegenseitiger Ausschluss
- gegenseitiger Ausschluss, Typen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da546c753696144c68348c61d01473c7d6414290b5971c220ac8c983317b3b15
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120110270"
---
# <a name="mutual-exclusion-types"></a>Gegenseitige Ausschlusstypen

Sie können typen des gegenseitigen Ausschlusses verwenden, um die Art eines gegenseitigen Ausschlussobjekts in einem Profil zu identifizieren. Gegenseitige Ausschlusstypen werden als Parameter für [**IWMMutualExclusion::GetType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmutualexclusion-gettype) und [**IWMMutualExclusion::SetType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmutualexclusion-settype)verwendet.

In der folgenden Tabelle sind die Bezeichner für gegenseitige Ausschlusstypen aufgeführt.



| Konstante des gegenseitigen Ausschlusstyps | GUID                                 |
|--------------------------------|--------------------------------------|
| CLSID \_ \_ WMMUTEX-Sprache       | D6E22A00-35DA-11D1-9034-00A0C90349BE |
| CLSID \_ \_ WMMUTEX-Bitrate        | D6E22A01-35DA-11D1-9034-00A0C90349BE |
| CLSID \_ WMMUTEX \_ Presentation   | D6E22A02-35DA-11D1-9034-00A0C90349BE |
| CLSID \_ WMMUTEX \_ Unbekannt        | D6E22A03-35DA-11D1-9034-00A0C90349BE |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**GUID-Werte**](guid-values.md)
</dt> </dl>

 

 




