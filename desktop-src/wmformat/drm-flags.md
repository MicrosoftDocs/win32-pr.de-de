---
title: DRM_Flags
description: Die EIGENSCHAFT DRM-Flags wird nur mit DRM-Inhalt der Version 1 verwendet, um die Rechte anzugeben, die \_ in der lokalen Lizenz enthalten sein werden.
ms.assetid: d9a776d3-da22-4111-b1ed-e3607a5576ef
keywords:
- DRM_Flags Windows-Medienformat
topic_type:
- apiref
api_name:
- DRM_Flags
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: adf4f1b2065eb1b251f0c555f8c33e424e43aefd04377ed894edb90c121aacb4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119086011"
---
# <a name="drm_flags"></a>\_DRM-Flags

Die **EIGENSCHAFT \_ DRM-Flags** wird nur mit DRM-Inhalt der Version 1 verwendet, um die Rechte anzugeben, die in der lokalen Lizenz enthalten sein werden. Rechte werden mit Werten angegeben, die vom **WMT \_ RIGHTS-Enumerationstyp** definiert werden. Mehrere Werte können ausgewählt werden, indem sie mit dem bitweise **OR-Operator kombiniert** werden.

## <a name="global-constant"></a>Globale Konstante

g \_ wszWMDRM-Flags \_

## <a name="data-type"></a>Datentyp

**WMT \_ TYPE \_ DWORD**

## <a name="remarks"></a>Hinweise

Wenn Sie auf die **IWMHeaderInfo3-Schnittstelle** des Writer-Objekts zugreifen, können Sie diesen Wert hinzufügen oder ändern. In anderen Objekten (Metadaten-Editor, Reader und synchroner Reader) ist dieser Wert schreibgeschützt. Verwenden [**Sie IWMHeaderInfo::SetAttribute,**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-setattribute) um diese Eigenschaft beim Erstellen von DRM-Inhalt der Version 1 festlegen.

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**DRM-Eigenschaften**](drm-properties.md)
</dt> </dl>

 

 




