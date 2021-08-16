---
title: IVMVirtualPC GetVirtualMachineFiles-Methode (VPCCOMInterfaces.h)
description: Ruft ein Array bekannter VM-Konfigurationsdateien ab.
ms.assetid: 38771573-66fa-408a-95db-1281efdf8b73
keywords:
- GetVirtualMachineFiles-Methode Virtueller PC
- GetVirtualMachineFiles-Methode Virtueller PC, IVMVirtualPC-Schnittstelle
- IVMVirtualPC-Schnittstelle Virtueller PC , GetVirtualMachineFiles-Methode
topic_type:
- apiref
api_name:
- IVMVirtualPC.GetVirtualMachineFiles
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64ae2f96fb0c289f155158c77cdf3e4a8df1cb83aa8a51e0329d9fcd835ea4d1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118998600"
---
# <a name="ivmvirtualpcgetvirtualmachinefiles-method"></a>IVMVirtualPC::GetVirtualMachineFiles-Methode

\[Windows Der virtuelle PC ist ab Windows 8 nicht mehr für die Verwendung verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Ruft ein Array bekannter VM-Konfigurationsdateien ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetVirtualMachineFiles(
  [in]          VARIANT      inAdditionalSearchPaths,
  [in]          VARIANT_BOOL inExcludedRegisteredVMs,
  [out, retval] VARIANT      *outVirtualMachineFileList
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*inAdditionalSearchPaths* \[ In\]
</dt> <dd>

Diese Pfade werden zusammen mit den Pfaden durchsucht, die in den Eigenschaften [**IVMVirtualPC::SearchPaths**](ivmvirtualpc-searchpaths.md) und [**IVMVirtualPC::D efaultVMConfigurationPath**](ivmvirtualpc-defaultvmconfigurationpath.md) festgelegt sind.

</dd> <dt>

*inExcludedRegisteredVMs* \[ In\]
</dt> <dd>

**TRUE,** wenn registrierte virtuelle Computer aus dem Array ausgeschlossen werden sollen, geben Sie im *outVirtualMachineFileList-Parameter* zurück, andernfalls **FALSE.**

</dd> <dt>

*outVirtualMachineFileList* \[ out, retval\]
</dt> <dd>

Ein Array von Pfadzeichenfolgen für die Konfigurationsdateien des virtuellen Computers, die in den angegebenen Suchpfaden gefunden werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode/-wert                                                                                                                                                                        | BESCHREIBUNG                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                              | Der Vorgang wurde durchgeführt.<br/>                                                        |
| <dl> <dt>**E \_ POINTER**</dt> <dt>0x80004003</dt> </dl>                                | Der *outVirtualMachineFileList-Parameter* ist **NULL.**<br/>                               |
| <dl> <dt>**E \_ INVALIDARG-0x80000003**</dt> <dt></dt> </dl>                             | Der *inAdditionalSearchPaths-Parameter* ist kein Array von Zeichenfolgen.<br/>                  |
| <dl> <dt>**DISP \_ E \_ EXCEPTION**</dt> <dt>0x80020009</dt> </dl>                        | Ein unerwarteter Fehler ist aufgetreten.<br/>                                                    |
| <dl> <dt>**VM \_ E \_ HARDWARE \_ VIRTUALIZATION \_ DISABLED**</dt> <dt>0xA0040951</dt> </dl> | Der Prozessor unterstützt keine HAV-Erweiterungen (Hardware Accelerated Virtualization).<br/> |



 

## <a name="remarks"></a>Hinweise

Die Suchpfade, die zum Abrufen des Arrays von Konfigurationsdateien verwendet werden, enthalten die zuvor von [**IVMVirtualPC::SearchPaths**](ivmvirtualpc-searchpaths.md) und [**IVMVirtualPC::D efaultVMConfigurationPath**](ivmvirtualpc-defaultvmconfigurationpath.md) festgelegten Pfade zusätzlich zu den durch den *InAdditionalSearchPaths-Parameter* angegebenen Pfaden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | nur Windows 7 \[ Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Product (Produkt)<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMVirtualPC ist als 236ba0d9-a24a-4292-a132-27c1421dfd01 definiert.<br/>               |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IVMVirtualPC**](ivmvirtualpc.md)
</dt> </dl>

 

