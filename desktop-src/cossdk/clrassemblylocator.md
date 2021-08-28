---
description: Ruft Informationen zu einer Assembly ab, wenn verwalteter Code in der .NET Framework Common Language Runtime verwendet wird.
ms.assetid: 45dcdc6a-74df-4763-ba8b-82f604db78d4
title: ClrAssemblyLocator-Klasse (ComSvcs.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ClrAssemblyLocator
api_type:
- COM
ms.openlocfilehash: 78f041e8bdc614b1ac6007e21ffbf46ea4afe789a501bb1acefdd21263031859
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119129272"
---
# <a name="clrassemblylocator-class"></a>ClrAssemblyLocator-Klasse

Ruft Informationen zu einer Assembly ab, wenn verwalteter Code in der .NET Framework Common Language Runtime verwendet wird.

## <a name="when-to-implement"></a>Gründe für die Implementierung

Diese Klasse wird von COM+ implementiert.



| Anforderung | Wert |
|------------|-------------------------------------------------------|
| CLSID      | GUID \_ AssemblyLocator                                 |
| ProgID     | L"System.EnterpriseServices.Internal.AssemblyLocator" |
| Schnittstellen | [**IAssemblyLocator**](/windows/desktop/api/ComSvcs/nn-comsvcs-iassemblylocator)          |



 

## <a name="when-to-use"></a>Verwendung

Verwenden Sie diese Klasse, um auf die Methoden von [**IAssemblyLocator**](/windows/desktop/api/ComSvcs/nn-comsvcs-iassemblylocator)zuzugreifen.

## <a name="remarks"></a>Hinweise

Um dieses Objekt zu erstellen, rufen Sie [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance)auf.

Um diese Klasse von Microsoft Visual Basic zu verwenden, fügen Sie einen Verweis auf die COM+-Diensttypbibliothek hinzu. Ein ClrAssemblyLocator-Objekt kann mit "COMSVCSLib.ClrAssemblyLocator" als Klassenname deklariert werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur XP mit \[ SP1-Desktop-Apps\]<br/>                                 |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>ComSvcs.h</dt> </dl> |



 

