---
description: Gibt an, ob die Komplexität des audiocodierungs Algorithmus eingeschränkt ist.
ms.assetid: a50b840f-9fe8-4291-b93f-f09c241fe802
title: MFPKEY_CONSTRAINENCOMPLEXITY-Eigenschaft (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bdc6e3d5a7077c72e5933ecbc235092174e263fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345889"
---
# <a name="mfpkey_constrainencomplexity-property"></a>Mfpkey- \_ einschränitäts Eigenschaft

Gibt an, ob die Komplexität des audiocodierungs Algorithmus eingeschränkt ist.

## <a name="constant-for-ipropertybag"></a>Konstante für IPropertyBag

Nur mit [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)verfügbar.

## <a name="data-type"></a>Datentyp

**VT \_ bool**

## <a name="default-value"></a>Standardwert

**Variant \_ false**

## <a name="remarks"></a>Bemerkungen

Wenn Sie für diese Eigenschaft den Standardwert **Variant \_ false** belassen, verwendet der Audioencoder seinen Standard Algorithmus. Der Standard Algorithmus hängt vom Ausgabetyp und der Version von Windows ab. In der folgenden Tabelle wird das Standardverhalten für die verschiedenen Kombinationen beschrieben.



| Betriebssystem | Standardverhalten                                                                                                                                                                                    |
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows Vista    | Für alle Ausgabetypen verwendet der Audioencoder standardmäßig den komplexesten Algorithmus.                                                                                                                 |
| Windows 7        | Bei Standard-und Professional-Ausgabetypen verwendet der Audioencoder standardmäßig den komplexesten Algorithmus. Für verlustfreie Ausgabetypen verwendet der Audioencoder standardmäßig den am wenigsten komplexen Algorithmus. |



 

Wenn Sie diese Eigenschaft auf **Variant \_ true** festlegen, müssen Sie auch einen Komplexitäts Wert angeben, indem Sie die Eigenschaft [**mfpkey \_ enckomplexewert**](mfpkey-enccomplexityproperty.md) festlegen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften von Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 
