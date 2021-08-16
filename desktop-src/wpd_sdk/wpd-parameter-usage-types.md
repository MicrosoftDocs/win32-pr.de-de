---
description: Der WPD \_ PARAMETER \_ USAGE \_ TYPES-Enumerationstyp beschreibt, wie ein Methodenparameter in einer bestimmten Methode verwendet wird.
ms.assetid: 60cbb4fa-c5fd-4402-bfd4-8fd95c009a33
title: WPD_PARAMETER_USAGE_TYPES -Enumeration (PortableDevice.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_PARAMETER_USAGE_TYPES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 8ece49d1b961ce6ce5c14241d14bf69480e1eb79028f57a2cb959f5d7c4b79dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117842067"
---
# <a name="wpd_parameter_usage_types-enumeration"></a>WPD \_ PARAMETER \_ USAGE \_ TYPES-Enumeration

Der [**WPD \_ PARAMETER USAGE \_ TYPES-Enumerationstyp \_**](/windows/desktop/wpd_sdk/wpd-parameter-usage-types) beschreibt, wie ein Methodenparameter in einer bestimmten Methode verwendet wird.

## <a name="syntax"></a>Syntax


```C++
typedef enum tagWPD_PARAMETER_USAGE_TYPES { 
  WPD_PARAMETER_USAGE_RETURN  = 0,
  WPD_PARAMETER_USAGE_IN      = 1,
  WPD_PARAMETER_USAGE_OUT     = 2,
  WPD_PARAMETER_USAGE_INOUT   = 3
} WPD_PARAMETER_USAGE_TYPES;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="WPD_PARAMETER_USAGE_RETURN"></span><span id="wpd_parameter_usage_return"></span>**\_ \_ WPD-PARAMETERVERWENDUNGS-RÜCKGABE \_**
</dt> <dd>

Der -Parameter empfängt den Rückgabewert, wenn er von der -Methode angegeben wird.

</dd> <dt>

<span id="WPD_PARAMETER_USAGE_IN"></span><span id="wpd_parameter_usage_in"></span>**\_WPD-PARAMETERVERWENDUNG \_ \_ IN**
</dt> <dd>

Der -Parameter enthält einen Eingabewert, bevor die -Methode aufgerufen wird.

</dd> <dt>

<span id="WPD_PARAMETER_USAGE_OUT"></span><span id="wpd_parameter_usage_out"></span>**\_WPD-PARAMETERVERWENDUNG \_ \_ OUT**
</dt> <dd>

Der -Parameter enthält einen Ausgabewert, wenn die Methode zurückgegeben wird.

</dd> <dt>

<span id="WPD_PARAMETER_USAGE_INOUT"></span><span id="wpd_parameter_usage_inout"></span>**\_WPD-PARAMETERVERWENDUNG \_ \_ INOUT**
</dt> <dd>

Der -Parameter enthält einen Eingabewert, bevor die Methode aufgerufen wird, und einen Ausgabewert, wenn sie zurückgegeben wird.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>PortableDevice.h</dt> </dl> |



 

