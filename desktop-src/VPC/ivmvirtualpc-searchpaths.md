---
title: Ivmvirtualpc SearchPath-Eigenschaft (vpccominterfaces. h)
description: Dateisystem Pfade, die verwendet werden, um Dateien zu suchen, die mit Windows Virtual PC verknüpft sind.
ms.assetid: 2a2deee5-7e6b-4b90-8ce9-0b0dbeef0f30
keywords:
- SearchPath-Eigenschaft virtueller PC
- SearchPath-Eigenschaft Virtual PC, ivmvirtualpc-Schnittstelle
- Ivmvirtualpc Interface Virtual PC, SearchPath (Eigenschaft)
topic_type:
- apiref
api_name:
- IVMVirtualPC.SearchPaths
- IVMVirtualPC.get_SearchPaths
- IVMVirtualPC.put_SearchPaths
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 287eb07bc9205f9b6f0851bd8809f9a49dcf3242
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103739745"
---
# <a name="ivmvirtualpcsearchpaths-property"></a>Ivmvirtualpc:: SearchPath (Eigenschaft)

\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Ruft die Dateisystem Pfade ab und legt Sie fest, die verwendet werden, um Dateien zu suchen, die mit Windows Virtual PC verknüpft sind.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_SearchPaths(
  [in]          VARIANT searchPaths
);

HRESULT get_SearchPaths(
  [out, retval] VARIANT *searchPaths
);
```



## <a name="property-value"></a>Eigenschaftswert

Gibt ein SAFEARRAY an, das für jeden Eintrag einen Dateisystempfad enthält.

## <a name="error-codes"></a>Fehlercodes



| Name/Wert                                                                                                                                                                               | Bedeutung                                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                                                  | Der Vorgang wurde durchgeführt.<br/>                                                                                               |
| <dl> <dt>E \_ Zeiger</dt> <dt>0x80004003</dt> </dl>                                    | Der-Parameter ist **null**.<br/>                                                                                                  |
| <dl> <dt>E \_ InvalidArg</dt> <dt>0x80000003</dt> </dl>                                 | Der *SearchPath* -Parameter ist ungültig und konnte nicht in ein Array von Pfaden analysiert werden.<br/>                                    |
| <dl> <dt>HRESULT \_ Von \_ Win32 (Fehler \_ Datei \_ nicht \_ gefunden)</dt> <dt>0x80070002</dt> </dl> | Das System kann ein im *SearchPath* -Parameter angegebenes Verzeichnis nicht finden.<br/>                                                |
| <dl> <dt>HRESULT \_ FROM \_ Win32 (Fehler \_ Pfad \_ nicht \_ gefunden)</dt> <dt>0x80070003</dt> </dl> | Das System kann keinen durch den *SearchPath* -Parameter angegebenen Pfad finden.<br/>                                                     |
| <dl> <dt>HRESULT \_ Von \_ Win32 ( \_ ungültiger \_ Name)</dt> <dt>0x8007007b</dt> </dl>    | Ein im *SearchPath* -Parameter angegebener Pfad enthält ungültige Zeichen. Ungültige Zeichen sind " \* ? <>/ \| ": ".<br/> |
| <dl> <dt>HRESULT \_ FROM \_ Win32 (Error ungültiger \_ \_ Pfadname)</dt> <dt>0x800700a1</dt> </dl>    | Ein im *SearchPath* -Parameter enthaltener Pfad gibt einen leeren oder relativen Pfad an. Ein absoluter Pfad ist erforderlich.<br/>          |
| <dl> <dt>HRESULT \_ Von \_ Win32 (Fehler \_ Puffer \_ Überlauf)</dt> <dt>0x8007006f</dt> </dl> | Der im *SearchPath* -Parameter angegebene Pfad ist zu lang. Die Länge des Pfads muss weniger als 260 Zeichen umfassen.<br/>     |
| <dl> <dt>VM \_ E \_ Pref \_ nicht \_ gefunden</dt> <dt>0xa0040300</dt> </dl>                       | Die Einstellung wurde nicht gefunden.<br/>                                                                                               |
| <dl> <dt>VM \_ E \_ \_ Hardwarevirtualisierung \_ deaktiviert</dt> <dt>0xa0040951</dt> </dl>     | Der Prozessor bietet keine Unterstützung für hav-Erweiterungen (Hardware Beschleunigung Virtualization).<br/>                                        |
| <dl> <dt>DISP \_ E- \_ Ausnahme</dt> <dt>0x80020009</dt> </dl>                            | Ein unerwarteter Fehler ist aufgetreten.<br/>                                                                                           |



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

 

