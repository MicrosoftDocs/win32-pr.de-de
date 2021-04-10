---
title: Ivmvirtualpc getconfigurationvalue-Methode (vpccominterfaces. h)
description: Ruft den Wert der angegebenen Konfigurationseinstellung ab
ms.assetid: 4598b57c-9942-4b40-97b5-41ad9ec74bfa
keywords:
- Getconfigurationvalue-Methode Virtual PC
- Getconfigurationvalue-Methode Virtual PC, ivmvirtualpc-Schnittstelle
- Ivmvirtualpc Interface Virtual PC, getconfigurationvalue-Methode
topic_type:
- apiref
api_name:
- IVMVirtualPC.GetConfigurationValue
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 11851e2dc2e51c0dc5eed876fc755655ed488554
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105200"
---
# <a name="ivmvirtualpcgetconfigurationvalue-method"></a>Ivmvirtualpc:: getconfigurationvalue-Methode

\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Ruft den Wert der angegebenen Konfigurationseinstellung ab

## <a name="syntax"></a>Syntax


```C++
HRESULT GetConfigurationValue(
  [in]          BSTR    preferenceKey,
  [out, retval] VARIANT *preferenceValue
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*preferecekey* \[ in\]
</dt> <dd>

Der Schlüssel, der verwendet wird, um die Einstellung zu identifizieren, wie Sie in der Konfigurationsdatei gespeichert ist.

</dd> <dt>

*preferumcevalue* \[ Out, retval\]
</dt> <dd>

Der bevorzugte Wert. Dieser Parameter kann einer der folgenden **Variant** -Typen sein: **VT \_ Array** \| **VT \_ UI1** (RAW Bytes), **VT \_ BSTR** (String), **VT \_ I4** (Integer) oder **VT \_ bool** (Boolean).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode/-wert                                                                                                                                                                        | BESCHREIBUNG                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                              | Der Vorgang wurde durchgeführt.<br/>                                                        |
| <dl> <dt>**E \_ Zeiger**</dt> <dt>0x80004003</dt> </dl>                                | Der *preferecekey* -Parameter oder der *preferendcevalue* -Parameter ist **null**.<br/>                      |
| <dl> <dt>**VM \_ E \_ Pref \_ nicht \_ gefunden**</dt> <dt>0xa0040300</dt> </dl>                   | Die Einstellung wurde nicht gefunden.<br/>                                                        |
| <dl> <dt>**VM \_ E \_ \_ Hardwarevirtualisierung \_ deaktiviert**</dt> <dt>0xa0040951</dt> </dl> | Der Prozessor bietet keine Unterstützung für hav-Erweiterungen (Hardware Beschleunigung Virtualization).<br/> |
| <dl> <dt>**DISP \_ E- \_ Ausnahme**</dt> <dt>0x80020009</dt> </dl>                        | Ein unerwarteter Fehler ist aufgetreten.<br/>                                                    |



 

## <a name="remarks"></a>Bemerkungen

Diese Methode ermöglicht den Zugriff auf niedriger Ebene auf einen beliebigen bevorzugten Wert für den aktuellen Benutzer. Sie kann verwendet werden, um bevorzugte Werte für Kunden definierte Schlüssel abzurufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Produkt<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>Vpccominterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ ivmvirtualpc ist als 236ba0d9-a24a-4292-A132-27c1421dfd01 definiert.<br/>               |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ivmvirtualpc**](ivmvirtualpc.md)
</dt> </dl>

 

