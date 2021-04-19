---
description: Der \_ Enumerationstyp der WPD-Parameter \_ Verwendungs \_ Typen beschreibt, wie ein Methoden Parameter in einer bestimmten Methode verwendet wird.
ms.assetid: 60cbb4fa-c5fd-4402-bfd4-8fd95c009a33
title: WPD_PARAMETER_USAGE_TYPES-Enumeration (portabledevice. h)
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
ms.openlocfilehash: 72d4ebffccc3d1bc7d446848c29ebbc60539430e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367642"
---
# <a name="wpd_parameter_usage_types-enumeration"></a>WPD- \_ Parameter \_ Verwendungs Typen- \_ Enumeration

Der Enumerationstyp der [**WPD- \_ Parameter \_ Verwendungs \_ Typen**](/windows/desktop/wpd_sdk/wpd-parameter-usage-types) beschreibt, wie ein Methoden Parameter in einer bestimmten Methode verwendet wird.

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

<span id="WPD_PARAMETER_USAGE_RETURN"></span><span id="wpd_parameter_usage_return"></span>**Verwendungs Rückgabe von WPD- \_ Parametern \_ \_**
</dt> <dd>

Der-Parameter empfängt den Rückgabewert, wenn er von der-Methode angegeben wird.

</dd> <dt>

<span id="WPD_PARAMETER_USAGE_IN"></span><span id="wpd_parameter_usage_in"></span>**Verwendung von WPD- \_ Parametern \_ \_ in**
</dt> <dd>

Der-Parameter enthält einen Eingabe Wert, bevor die-Methode aufgerufen wird.

</dd> <dt>

<span id="WPD_PARAMETER_USAGE_OUT"></span><span id="wpd_parameter_usage_out"></span>**Verwendung von WPD- \_ Parametern \_ \_**
</dt> <dd>

Der-Parameter enthält einen Ausgabewert, wenn die-Methode zurückgibt.

</dd> <dt>

<span id="WPD_PARAMETER_USAGE_INOUT"></span><span id="wpd_parameter_usage_inout"></span>**\_ \_ INOUT-Verwendung \_ von WPD-Parametern**
</dt> <dd>

Der-Parameter enthält einen Eingabe Wert, bevor die-Methode aufgerufen wird, und einen Ausgabewert, wenn Sie zurückgibt.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Portabledevice. h</dt> </dl> |



 

