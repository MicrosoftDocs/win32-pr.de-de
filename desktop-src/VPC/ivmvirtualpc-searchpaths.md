---
title: IVMVirtualPC SearchPaths-Eigenschaft (VPCCOMInterfaces.h)
description: Dateisystempfade, die zum Suchen von Dateien verwendet werden, die dem virtuellen Windows zugeordnet sind.
ms.assetid: 2a2deee5-7e6b-4b90-8ce9-0b0dbeef0f30
keywords:
- SearchPaths-Eigenschaft Virtueller PC
- SearchPaths-Eigenschaft Virtueller PC, IVMVirtualPC-Schnittstelle
- IVMVirtualPC-Schnittstelle Virtueller PC, SearchPaths-Eigenschaft
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
ms.openlocfilehash: ac4ef75bf0a696494b839f330063ca310927a0d796829d96575721f492b8b691
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119471250"
---
# <a name="ivmvirtualpcsearchpaths-property"></a>IVMVirtualPC::SearchPaths-Eigenschaft

\[Windows Der virtuelle PC ist ab diesem Zeitraum nicht mehr Windows 8. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Ruft die Dateisystempfade ab, die zum Suchen von Dateien verwendet werden, die dem virtuellen Windows zugeordnet sind, und legt diese fest.

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

Gibt ein safearray an, das einen Dateisystempfad für jeden Eintrag enthält.

## <a name="error-codes"></a>Fehlercodes



| Name/Wert                                                                                                                                                                               | Bedeutung                                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                                                  | Der Vorgang wurde durchgeführt.<br/>                                                                                               |
| <dl> <dt>E \_ ZEIGER 0X80004003</dt> <dt></dt> </dl>                                    | Der Parameter ist **NULL.**<br/>                                                                                                  |
| <dl> <dt>E \_ INVALIDARG-0x80000003</dt> <dt></dt> </dl>                                 | Der *searchPaths-Parameter* ist ungültig und konnte nicht in ein Array von Pfaden analysiert werden.<br/>                                    |
| <dl> <dt>HRESULT \_ FROM \_ WIN32(ERROR \_ FILE NOT \_ \_ FOUND)</dt> <dt>0X80070002</dt> </dl> | Das System kann kein im *searchPaths-Parameter angegebenes Verzeichnis* finden.<br/>                                                |
| <dl> <dt>HRESULT \_ FROM \_ WIN32(ERROR \_ PATH NOT \_ \_ FOUND)</dt> <dt>0x80070003</dt> </dl> | Das System kann keinen pfad finden, der durch den *searchPaths-Parameter angegeben* wird.<br/>                                                     |
| <dl> <dt>HRESULT \_ FROM \_ WIN32(ERROR \_ INVALID \_ NAME)</dt> <dt>0x8007007b</dt> </dl>    | Ein im *searchPaths-Parameter angegebener* Pfad enthält unzulässige Zeichen. Die unzulässigen Zeichen sind " \* ?<>/ \| ":".<br/> |
| <dl> <dt>HRESULT \_ FROM \_ WIN32(ERROR \_ BAD \_ PATHNAME)</dt> <dt>0x800700a1</dt> </dl>    | Ein im *searchPaths-Parameter enthaltener* Pfad gibt einen leeren oder relativen Pfad an. Ein absoluter Pfad ist erforderlich.<br/>          |
| <dl> <dt>HRESULT \_ FROM \_ WIN32(ERROR \_ BUFFER \_ OVERFLOW)</dt> <dt>0x8007006f</dt> </dl> | Der im *searchPaths-Parameter angegebene* Pfad ist zu lang. Die Länge des Pfads muss weniger als 260 Zeichen umfassen.<br/>     |
| <dl> <dt>VM \_ E \_ PREF \_ NOT \_ FOUND</dt> <dt>0xA0040300</dt> </dl>                       | Die Einstellung wurde nicht gefunden.<br/>                                                                                               |
| <dl> <dt>VM \_ E \_ \_ HARDWAREVIRTUALISIERUNG \_ DEAKTIVIERT</dt> <dt>0XA0040951</dt> </dl>     | Der Prozessor unterstützt keine HAV-Erweiterungen (Hardware Accelerated Virtualization).<br/>                                        |
| <dl> <dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt> </dl>                            | Ein unerwarteter Fehler ist aufgetreten.<br/>                                                                                           |



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

 

