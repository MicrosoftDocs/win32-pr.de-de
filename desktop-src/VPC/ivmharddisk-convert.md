---
title: IVMHardDisk Convert-Methode (VPCCOMInterfaces.h)
description: Konvertiert eine virtuelle Festplatte mit fester Größe in eine dynamisch erweiterbare virtuelle Festplatte oder konvertiert eine dynamisch erweiterbare virtuelle Festplatte in eine virtuelle Festplatte mit fester Größe.
ms.assetid: 0dee802a-1cac-499e-918a-7dbb6c98415f
keywords:
- Convert method Virtual PC
- Convert method Virtual PC , IVMHardDisk interface
- IVMHardDisk-Schnittstelle Virtueller PC, Convert-Methode
topic_type:
- apiref
api_name:
- IVMHardDisk.Convert
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e509c683ef86e169eb07d661c9682d8ed67204bcc7e1651d2d6370ee4be82f09
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118593883"
---
# <a name="ivmharddiskconvert-method"></a>IVMHardDisk::Convert-Methode

\[Windows Der virtuelle PC ist ab Windows 8 nicht mehr für die Verwendung verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Konvertiert eine virtuelle Festplatte mit fester Größe in eine dynamisch erweiterbare virtuelle Festplatte oder konvertiert eine dynamisch erweiterbare virtuelle Festplatte in eine virtuelle Festplatte mit fester Größe.

## <a name="syntax"></a>Syntax


```C++
HRESULT Convert(
  [in]          BSTR           convertedDiskImagePath,
  [in]          VMHardDiskType convertedDiskImageType,
  [out, retval] IVMTask        **convertTask
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*convertedDiskImagePath* \[ In\]
</dt> <dd>

Der Pfad zur Zieldatenträger-Imagedatei.

</dd> <dt>

*convertedDiskImageType* \[ In\]
</dt> <dd>

Der Typ des Zieldatenträgerimages. Eine Liste der Werte finden Sie unter [**VMHardDiskType.**](vmharddisktype.md)

</dd> <dt>

*convertTask* \[ out, retval\]
</dt> <dd>

Ein [**IVMTask-Objekt,**](ivmtask.md) das zum Nachverfolgen des Abschlusses des Konvertierungsprozesses verwendet wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode/-wert                                                                                                                                                                              | BESCHREIBUNG                                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                                    | Der Vorgang wurde durchgeführt.<br/>                                                                                                        |
| <dl> <dt>**E \_ INVALIDARG-0x80000003**</dt> <dt></dt> </dl>                                   | Der *convertedDiskImagePath-Parameter* ist leer oder enthält keine VHD-Erweiterung für den Dateinamen.<br/>                                      |
| <dl> <dt>**E \_ POINTER**</dt> <dt>0x80004003</dt> </dl>                                      | Ein Parameter ist **NULL.**<br/>                                                                                                             |
| <dl> <dt>**HRESULT \_ FROM \_ WIN32(ERROR \_ PATH NOT \_ \_ FOUND)**</dt> <dt>0x80070003</dt> </dl>   | Das System kann den vom *convertedDiskImagePath-Parameter* angegebenen Pfad nicht finden.<br/>                                                 |
| <dl> <dt>**HRESULT \_ FROM \_ WIN32(ERROR \_ INVALID \_ NAME)**</dt> <dt>0x8007007b</dt> </dl>      | Der *convertedDiskImagePath-Parameter* enthält ein ungültiges Zeichen (eines von " \* ?<>/ \| ":").<br/>                                    |
| <dl> <dt>**HRESULT \_ FROM \_ WIN32(ERROR \_ BAD \_ PATHNAME)**</dt> <dt>0x800700a1</dt> </dl>      | Der *convertedDiskImagePath-Parameter* gibt einen leeren oder relativen Pfad an. Ein absoluter Pfad ist erforderlich.<br/>                            |
| <dl> <dt>**HRESULT \_ FROM \_ WIN32(ERROR \_ BUFFER \_ OVERFLOW)**</dt> <dt>0x8007006f</dt> </dl>   | Der vom *convertedDiskImagePath-Parameter* angegebene Pfad ist zu lang. Der Pfad muss kleiner als **MAX \_ PATH** (260) Zeichen sein.<br/> |
| <dl> <dt>**HRESULT \_ FROM \_ WIN32(ERROR \_ SHARING \_ VIOLATION)**</dt> <dt>0x80070020</dt> </dl> | Entweder wird die virtuelle Festplatte verwendet, auf die dieses Objekt verweist, oder das übergeordnete Element dieser virtuellen Festplatte wird verwendet.<br/>                  |
| <dl> <dt>**HRESULT \_ FROM \_ WIN32(ERROR \_ DISK \_ FULL)**</dt> <dt>0x80070070</dt> </dl>         | Das Hostvolume verfügt nicht über genügend Speicherplatz zum Konvertieren dieser virtuellen Festplatte.<br/>                                                        |
| <dl> <dt>**HRESULT \_ VON \_ WIN32(FEHLER \_ IST BEREITS \_ VORHANDEN)**</dt> <dt>0X800700B7</dt> </dl>    | Die Datei, auf die der *convertedDiskImagePath-Parameter* verweist, ist bereits vorhanden.<br/>                                                        |
| <dl> <dt>**VM \_ E \_ WRONG HD IMAGE \_ \_ \_ TYPE**</dt> <dt>0xA004067B</dt> </dl>                   | Der *convertedDiskImagePath-Parameter* muss entweder **vmDiskType \_ Dynamic** oder **vmDiskType \_ FixedSize** sein.<br/>                          |
| <dl> <dt>**VM \_ E \_ INVALID \_ HD \_ FILE**</dt> <dt>0xA0040682</dt> </dl>                        | Das image der virtuellen Festplatte, auf das dieses [**IVMHardDisk-Objekt**](ivmharddisk.md) verweist, scheint kein gültiges Image zu sein.<br/>          |
| <dl> <dt>**VM \_ \_E \_ ÜBERGEORDNETER PFAD \_ NICHT \_ GEFUNDEN**</dt> <dt>0XA0040677</dt> </dl>                 | Das übergeordnete Element der virtuellen Festplatte, auf die dieses Objekt verweist, ist nicht vorhanden.<br/>                                                        |
| <dl> <dt>**VM \_ E \_ APP \_ SHUTING \_ DOWN**</dt> <dt>0xA0040209</dt> </dl>                      | Das image der virtuellen Festplatte kann nicht konvertiert werden, da die Anwendung heruntergefahren wird.<br/>                                            |
| <dl> <dt>**DISP \_ E \_ EXCEPTION**</dt> <dt>0x80020009</dt> </dl>                              | Ein unerwarteter Fehler ist aufgetreten.<br/>                                                                                                    |



 

## <a name="remarks"></a>Bemerkungen

Die Quelldatei bleibt nach dem Konvertierungsprozess intakt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | nur Windows 7 \[ Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Produkt<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMHardDisk ist als ffa14ae6-48f5-42a4-8a22-186f2e5c7db0 definiert.<br/>                |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IVMHardDisk**](ivmharddisk.md)
</dt> </dl>

 

