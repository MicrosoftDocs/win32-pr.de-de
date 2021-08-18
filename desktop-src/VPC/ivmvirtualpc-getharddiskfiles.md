---
title: IVMVirtualPC GetHardDiskFiles-Methode (VPCCOMInterfaces.h)
description: Ruft ein Array bekannter virtueller Festplattendateien ab.
ms.assetid: 3f949ebc-5974-4919-84a2-8411f558f85f
keywords:
- GetHardDiskFiles-Methode Virtueller PC
- GetHardDiskFiles-Methode Virtueller PC, IVMVirtualPC-Schnittstelle
- IVMVirtualPC-Schnittstelle Virtueller PC, GetHardDiskFiles-Methode
topic_type:
- apiref
api_name:
- IVMVirtualPC.GetHardDiskFiles
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 902cd124db27ae65b8f589ded8b2b3188a7e0df67b0ff20071abd04daf5ab894
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119136573"
---
# <a name="ivmvirtualpcgetharddiskfiles-method"></a>IVMVirtualPC::GetHardDiskFiles-Methode

\[Windows Der virtuelle PC ist ab diesem Zeitraum nicht mehr Windows 8. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Ruft ein Array bekannter virtueller Festplattendateien ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetHardDiskFiles(
  [in]          VARIANT inAdditionalSearchPaths,
  [out, retval] VARIANT *outHardDiskFileList
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*inAdditionalSearchPaths* \[ In\]
</dt> <dd>

Diese Pfade werden zusammen mit den In der [**IVMVirtualPC::SearchPaths-Eigenschaft festgelegten Pfaden durchsucht.**](ivmvirtualpc-searchpaths.md)

</dd> <dt>

*outHardDiskFileList* \[ out, retval\]
</dt> <dd>

Ein Array von Pfadzeichenfolgen für die virtuellen Festplattendateien, die in den angegebenen Suchpfaden gefunden werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode/-wert                                                                                                                                                                        | Beschreibung                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                              | Der Vorgang wurde durchgeführt.<br/>                                                        |
| <dl> <dt>**E \_ ZEIGER 0X80004003**</dt> <dt></dt> </dl>                                | Der *outHardDiskFileList-Parameter* ist **NULL.**<br/>                                     |
| <dl> <dt>**E \_ INVALIDARG-0x80000003**</dt> <dt></dt> </dl>                             | Der *parameter inAdditionalSearchPaths* ist kein Array von Zeichenfolgen.<br/>                  |
| <dl> <dt>**DISP \_ E \_ EXCEPTION**</dt> <dt>0x80020009</dt> </dl>                        | Ein unerwarteter Fehler ist aufgetreten.<br/>                                                    |
| <dl> <dt>**VM \_ E \_ \_ HARDWAREVIRTUALISIERUNG \_ DEAKTIVIERT**</dt> <dt>0XA0040951</dt> </dl> | Der Prozessor unterstützt keine HAV-Erweiterungen (Hardware Accelerated Virtualization).<br/> |



 

## <a name="remarks"></a>Hinweise

Die Suchpfade, die zum Abrufen des Arrays von Dateien verwendet werden, enthalten die zuvor von [**IVMVirtualPC::SearchPaths**](ivmvirtualpc-searchpaths.md) festgelegten Pfade zusätzlich zu den durch den *parameter inAdditionalSearchPaths* angegebenen Pfaden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Product (Produkt)<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMVirtualPC ist als 236ba0d9-a24a-4292-a132-27c1421dfd01 definiert.<br/>               |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IVMVirtualPC**](ivmvirtualpc.md)
</dt> </dl>

 

