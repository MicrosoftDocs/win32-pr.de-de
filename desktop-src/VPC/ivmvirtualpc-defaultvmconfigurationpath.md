---
title: Ivmvirtualpc defaultvmconfigurationpath-Eigenschaft (vpccominterfaces. h)
description: Standardverzeichnis, das nach verfügbaren Konfigurationsdateien für virtuelle Maschinen durchsucht werden soll.
ms.assetid: 9ae63198-e3f6-4dcb-8edb-85adfbbdca26
keywords:
- Defaultvmconfigurationpath-Eigenschaft virtueller PC
- Defaultvmconfigurationpath-Eigenschaft Virtual PC, ivmvirtualpc-Schnittstelle
- Ivmvirtualpc Interface Virtual PC, defaultvmconfigurationpath (Eigenschaft)
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
ms.openlocfilehash: e13fc2323cb15bdbeb8c42e61810a376e49b3988
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742729"
---
# <a name="ivmvirtualpcdefaultvmconfigurationpath-property"></a>Ivmvirtualpc::D efaultvmconfigurationpath-Eigenschaft

\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Ruft das Standardverzeichnis ab, das nach verfügbaren Konfigurationsdateien für virtuelle Maschinen gesucht werden soll, und legt dieses fest.

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

Gibt den Verzeichnispfad für die Standard Konfigurationsdateien der virtuellen Maschine an. In der Pfad Zeichenfolge wird ein umgekehrter Schrägstrich ( \) möglicherweise direkt vor dem abschließenden NULL-Zeichen angezeigt).

## <a name="error-codes"></a>Fehlercodes



| Name/Wert                                                                                                                                                                               | Bedeutung                                                                                                                                                  |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                                                  | Der Vorgang wurde durchgeführt.<br/>                                                                                                                 |
| <dl> <dt>E \_ Zeiger</dt> <dt>0x80004003</dt> </dl>                                    | Der *ConfigurationPath* -Parameter ist **null**.<br/>                                                                                                |
| <dl> <dt>HRESULT \_ Von \_ Win32 (Fehler \_ Datei \_ nicht \_ gefunden)</dt> <dt>0x80070002</dt> </dl> | Das System kann das vom *ConfigurationPath* -Parameter angegebene Verzeichnis nicht finden.<br/>                                                          |
| <dl> <dt>HRESULT \_ FROM \_ Win32 (Fehler \_ Pfad \_ nicht \_ gefunden)</dt> <dt>0x80070003</dt> </dl> | Das System kann den vom *ConfigurationPath* -Parameter angegebenen Pfad nicht finden.<br/>                                                               |
| <dl> <dt>HRESULT \_ Von \_ Win32 ( \_ ungültiger \_ Name)</dt> <dt>0x8007007b</dt> </dl>    | Der *ConfigurationPath* -Parameter enthält ein ungültiges Zeichen (eines der folgenden Zeichen: " \* ? <>/ \| ": ").<br/>                                   |
| <dl> <dt>HRESULT \_ FROM \_ Win32 (Error ungültiger \_ \_ Pfadname)</dt> <dt>0x800700a1</dt> </dl>    | Der *ConfigurationPath* -Parameter gibt einen leeren oder relativen Pfad an. Ein absoluter Pfad ist erforderlich.<br/>                                          |
| <dl> <dt>HRESULT \_ Von \_ Win32 (Fehler \_ Puffer \_ Überlauf)</dt> <dt>0x8007006f</dt> </dl> | Der vom *ConfigurationPath* -Parameter angegebene Pfad ist zu lang. Die Länge des Pfads muss kleiner als der **Maximale \_ Pfad** (260) sein.<br/> |
| <dl> <dt>DISP \_ E- \_ Ausnahme</dt> <dt>0x80020009</dt> </dl>                            | Ein unerwarteter Fehler ist aufgetreten.<br/>                                                                                                             |
| <dl> <dt>VM \_ E \_ \_ Hardwarevirtualisierung \_ deaktiviert</dt> <dt>0xa0040951</dt> </dl>     | Der Prozessor bietet keine Unterstützung für hav-Erweiterungen (Hardware Beschleunigung Virtualization).<br/>                                                          |



## <a name="remarks"></a>Bemerkungen

Standardmäßig ist dieser Eigenschafts Wert auf das folgende Verzeichnis festgelegt: "% LocalAppData% \\ Microsoft \\ Windows Virtual PC \\ Virtual Machines \\ ".

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

 

