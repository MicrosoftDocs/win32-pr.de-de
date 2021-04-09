---
title: DRM_Flags
description: Die DRM- \_ Flags-Eigenschaft wird nur mit DRM-Inhalt der Version 1 verwendet, um die Rechte anzugeben, die in der lokalen Lizenz enthalten sein werden.
ms.assetid: d9a776d3-da22-4111-b1ed-e3607a5576ef
keywords:
- DRM_Flags Windows Media-Format
topic_type:
- apiref
api_name:
- DRM_Flags
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b4f2f8eb2baa401f1bc8519da5ca555a1fe428ee
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "103948429"
---
# <a name="drm_flags"></a>DRM- \_ Flags

Die **DRM- \_ Flags** -Eigenschaft wird nur mit DRM-Inhalt der Version 1 verwendet, um die Rechte anzugeben, die in der lokalen Lizenz enthalten sein werden. Rechte werden mit Werten angegeben, die durch den Enumerationstyp **WMT- \_ Rechte** definiert werden. Es können mehrere Werte ausgewählt werden, indem Sie mit dem bitweisen **or** -Operator kombiniert werden.

## <a name="global-constant"></a>Globale Konstante

g \_ wszwmdrm- \_ Flags

## <a name="data-type"></a>Datentyp

**WMT- \_ Typ \_ DWORD**

## <a name="remarks"></a>Bemerkungen

Beim Zugriff auf die **IWMHeaderInfo3** -Schnittstelle des Writer-Objekts können Sie diesen Wert hinzufügen oder ändern. In anderen Objekten (Metadaten-Editor, Reader und synchroner Reader) ist dieser Wert schreibgeschützt. Verwenden Sie [**iwmheaderinfo:: setAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-setattribute) , um diese Eigenschaft beim Erstellen von DRM-Version 1-Inhalten festzulegen.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**DRM-Eigenschaften**](drm-properties.md)
</dt> </dl>

 

 




