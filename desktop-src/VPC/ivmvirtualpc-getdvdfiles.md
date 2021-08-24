---
title: IVMVirtualPC GetDVDFiles-Methode (VPCCOMInterfaces.h)
description: Ruft ein Array bekannter DVD-Dateien ab.
ms.assetid: 9fe2191f-c5c0-464d-a190-29b2aba69682
keywords:
- GetDVDFiles-Methode Virtueller PC
- GetDVDFiles-Methode Virtual PC , IVMVirtualPC-Schnittstelle
- IVMVirtualPC-Schnittstelle Virtueller PC, GetDVDFiles-Methode
topic_type:
- apiref
api_name:
- IVMVirtualPC.GetDVDFiles
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 585b1558c5a0692d4f9a3d5d8371cd0b7e5a692596c06605e7d86eadf377cf45
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119864120"
---
# <a name="ivmvirtualpcgetdvdfiles-method"></a>IVMVirtualPC::GetDVDFiles-Methode

\[Windows Der virtuelle PC ist ab Windows 8 nicht mehr für die Verwendung verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Ruft ein Array bekannter DVD-Dateien ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetDVDFiles(
  [in]          VARIANT inAdditionalSearchPaths,
  [out, retval] VARIANT *outDVDFileList
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*inAdditionalSearchPaths* \[ In\]
</dt> <dd>

Diese Pfade werden zusammen mit den Pfaden durchsucht, die in der [**IVMVirtualPC::SearchPaths-Eigenschaft**](ivmvirtualpc-searchpaths.md) festgelegt sind.

</dd> <dt>

*outDVDFileList* \[ out, retval\]
</dt> <dd>

Ein Array von virtuellen DVD-Dateien, die in den angegebenen Suchpfaden gefunden wurden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode/-wert                                                                                                                                                                        | BESCHREIBUNG                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                              | Der Vorgang wurde durchgeführt.<br/>                                                        |
| <dl> <dt>**E \_ POINTER**</dt> <dt>0x80004003</dt> </dl>                                | Der *outDVDFileList-Parameter* ist **NULL.**<br/>                                          |
| <dl> <dt>**E \_ INVALIDARG-0x80000003**</dt> <dt></dt> </dl>                             | Der *inAdditionalSearchPaths-Parameter* ist kein Array von Zeichenfolgen.<br/>                  |
| <dl> <dt>**DISP \_ E \_ EXCEPTION**</dt> <dt>0x80020009</dt> </dl>                        | Ein unerwarteter Fehler ist aufgetreten.<br/>                                                    |
| <dl> <dt>**VM \_ E \_ \_ HARDWAREVIRTUALISIERUNG \_ DEAKTIVIERT**</dt> <dt>0xA0040951</dt> </dl> | Der Prozessor unterstützt keine HAV-Erweiterungen (Hardware Accelerated Virtualization).<br/> |



 

## <a name="remarks"></a>Hinweise

Die Suchpfade, die zum Abrufen des Dateiarrays verwendet werden, enthalten die zuvor von [**IVMVirtualPC::SearchPaths**](ivmvirtualpc-searchpaths.md) festgelegten Zusätzlich zu den durch den *inAdditionalSearchPaths-Parameter* und den Installationsprogrammspeicherort für das Integrationskomponentenmodul angegebenen Pfaden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | nur Windows 7 \[ Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Product (Produkt)<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMVirtualPC ist als 236ba0d9-a24a-4292-a132-27c1421dfd01 definiert.<br/>               |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IVMVirtualPC**](ivmvirtualpc.md)
</dt> </dl>

 

