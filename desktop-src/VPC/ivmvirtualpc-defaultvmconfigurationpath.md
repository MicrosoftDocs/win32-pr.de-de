---
title: IVMVirtualPC DefaultVMConfigurationPath-Eigenschaft (VPCCOMInterfaces.h)
description: Standardverzeichnis, das nach verfügbaren Konfigurationsdateien für virtuelle Computer durchsucht werden soll.
ms.assetid: 9ae63198-e3f6-4dcb-8edb-85adfbbdca26
keywords:
- DefaultVMConfigurationPath-Eigenschaft Virtueller PC
- DefaultVMConfigurationPath-Eigenschaft Virtueller PC, IVMVirtualPC-Schnittstelle
- IVMVirtualPC-Schnittstelle Virtueller PC, DefaultVMConfigurationPath-Eigenschaft
topic_type:
- apiref
api_name:
- IVMVirtualPC.DefaultVMConfigurationPath
- IVMVirtualPC.get_DefaultVMConfigurationPath
- IVMVirtualPC.put_DefaultVMConfigurationPath
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09f6370dfb868ec386e05f361240a74412f13a7d
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111387636"
---
# <a name="ivmvirtualpcdefaultvmconfigurationpath-property"></a>IVMVirtualPC::D efaultVMConfigurationPath (Eigenschaft)

\[Der virtuelle Windows-PC kann ab diesem Windows 8. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Ruft das Standardverzeichnis ab, das nach verfügbaren Konfigurationsdateien für virtuelle Computer durchsucht werden soll, und legt es fest.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_DefaultVMConfigurationPath(
  [in]          BSTR configurationPath
);

HRESULT get_DefaultVMConfigurationPath(
  [out, retval] BSTR *configurationPath
);
```



## <a name="property-value"></a>Eigenschaftswert

Gibt den Verzeichnispfad für die Standardkonfigurationsdateien des virtuellen Computers an. In der Pfadzeichenfolge kann ein zurücker Schrägstrich ( ) unmittelbar vor dem beendenden \\ NULL-Zeichen angezeigt werden.

## <a name="error-codes"></a>Fehlercodes



| Name/Wert                                                                                                                                                                               | Bedeutung                                                                                                                                                  |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                                                  | Der Vorgang wurde durchgeführt.<br/>                                                                                                                 |
| <dl> <dt>E \_ ZEIGER 0X80004003</dt> <dt></dt> </dl>                                    | Der *configurationPath-Parameter* ist **NULL.**<br/>                                                                                                |
| <dl> <dt>HRESULT \_ FROM \_ WIN32(ERROR \_ FILE NOT \_ \_ FOUND)</dt> <dt>0X80070002</dt> </dl> | Das vom configurationPath-Parameter angegebene Verzeichnis kann vom *System nicht finden.*<br/>                                                          |
| <dl> <dt>HRESULT \_ FROM \_ WIN32(ERROR \_ PATH NOT \_ \_ FOUND)</dt> <dt>0x80070003</dt> </dl> | Das System kann den durch den *configurationPath-Parameter angegebenen Pfad nicht* finden.<br/>                                                               |
| <dl> <dt>HRESULT \_ FROM \_ WIN32(ERROR \_ INVALID \_ NAME)</dt> <dt>0x8007007b</dt> </dl>    | Der *parameter configurationPath* enthält ein ungültiges Zeichen (eines der folgenden Zeichen: " \* ?<>/ \| ":").<br/>                                   |
| <dl> <dt>HRESULT \_ FROM \_ WIN32(ERROR \_ BAD \_ PATHNAME)</dt> <dt>0x800700a1</dt> </dl>    | Der *configurationPath-Parameter* gibt einen leeren oder relativen Pfad an. Ein absoluter Pfad ist erforderlich.<br/>                                          |
| <dl> <dt>HRESULT \_ FROM \_ WIN32(ERROR \_ BUFFER \_ OVERFLOW)</dt> <dt>0x8007006f</dt> </dl> | Der vom *configurationPath-Parameter angegebene Pfad* ist zu lang. Die Länge des Pfads muss kleiner als **MAX \_ PATH** (260) Zeichen sein.<br/> |
| <dl> <dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt> </dl>                            | Ein unerwarteter Fehler ist aufgetreten.<br/>                                                                                                             |
| <dl> <dt>VM \_ E \_ \_ HARDWAREVIRTUALISIERUNG \_ DEAKTIVIERT</dt> <dt>0XA0040951</dt> </dl>     | Der Prozessor unterstützt keine HAV-Erweiterungen (Hardware Accelerated Virtualization).<br/>                                                          |



## <a name="remarks"></a>Hinweise

Standardmäßig ist dieser Eigenschaftswert auf das folgende Verzeichnis festgelegt: "%LocalAppData% \\ Microsoft Windows Virtual PC Virtual Machines \\ \\ \\ ".

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows \[ 7-Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Produkt<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMVirtualPC ist als 236ba0d9-a24a-4292-a132-27c1421dfd01 definiert.<br/>               |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IVMVirtualPC**](ivmvirtualpc.md)
</dt> </dl>

 

