---
description: Die Directory-Methode ruft eine Liste von Dateien des angegebenen Typs aus dem aktuellen Verzeichnis ab.
ms.assetid: 0ae89811-7534-497b-af9f-ae37a48bc3e5
title: ISCardFileAccess::D-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardFileAccess.Directory
api_type:
- COM
api_location: ''
ms.openlocfilehash: 009263a92f014367636c7ff16b7f43635f73fa1b2ed17b52d53e81152c6e15b6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119481300"
---
# <a name="iscardfileaccessdirectory-method"></a>ISCardFileAccess::D-Methode

\[Die **Directory-Methode** ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt Anforderungen angegeben sind. Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die [Smartcardmodule](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten ähnliche Funktionen.\]

Die **Directory-Methode** ruft eine Liste von Dateien des angegebenen Typs aus dem aktuellen Verzeichnis ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT Directory(
  [in]  FILETYPE    fileType,
  [out] LPSAFEARRAY *ppFileList
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*fileType* \[ In\]
</dt> <dd>

Typ der [*auflistenden*](../secgloss/s-gly.md) Smartcarddateien.



| Wert                                                                                                                                                                                      | Bedeutung                                              |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <span id="SC_TYPE_DIRECTORIES"></span><span id="sc_type_directories"></span><dl> <dt>**\_ \_ SC-TYPVERZEICHNISSE**</dt> </dl>           | Nur Verzeichnisdateien auflisten.<br/>                |
| <span id="SC_TYPE_FILES"></span><span id="sc_type_files"></span><dl> <dt>**\_ \_ SC-TYPDATEIEN**</dt> </dl>                             | Nur elementare Dateien auflisten.<br/>               |
| <span id="SC_TYPE_ALL_FILES"></span><span id="sc_type_all_files"></span><dl> <dt>**SC \_ TYPE \_ ALL \_ FILES**</dt> </dl>                | Listen Sie sowohl Verzeichnisdateien als auch elementare Dateien auf.<br/> |
| <span id="SC_TYPE_DIRECTORY_FILE"></span><span id="sc_type_directory_file"></span><dl> <dt>**VERZEICHNISDATEI \_ DES \_ \_ SC-TYPS**</dt> </dl> | Verzeichnisdatei.<br/>                           |
| <span id="SC_TYPE_TRANSPARENT_EF"></span><span id="sc_type_transparent_ef"></span><dl> <dt>**SC \_ TYPE \_ TRANSPARENT \_ EF**</dt> </dl> | Transparente elementare Datei.<br/>              |
| <span id="SC_TYPE_FIXED_EF"></span><span id="sc_type_fixed_ef"></span><dl> <dt>**SC \_ TYPE \_ FIXED \_ EF**</dt> </dl>                   | Lineare feste elementare Datei.<br/>             |
| <span id="SC_TYPE_CYCLIC_EF"></span><span id="sc_type_cyclic_ef"></span><dl> <dt>**SC \_ TYPE \_ CYCLIC \_ EF**</dt> </dl>                | Zyklische elementare Datei.<br/>                   |
| <span id="SC_TYPE_VARIABLE_EF"></span><span id="sc_type_variable_ef"></span><dl> <dt>**SC \_ TYPE \_ VARIABLE \_ EF**</dt> </dl>          | Lineare Variable elementare Datei.<br/>          |



 

</dd> <dt>

*ppFileList* \[ out\]
</dt> <dd>

Array von BSTRs, das die Liste der Dateien darstellt, die mit dem Spezifizierer in *fileType übereinstimmen.*

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die -Methode gibt einen der folgenden möglichen Werte zurück.



| Rückgabecode                                                                                   | Beschreibung                                               |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Der Vorgang wurde erfolgreich abgeschlossen.<br/>          |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Ungültiger Parameter.<br/>                             |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>     | Die -Schnittstelle hat diese Methode nicht implementiert.<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Nicht genügend Arbeitsspeicher.<br/>                                 |
| <dl> <dt>**\_E-ZEIGER**</dt> </dl>     | Für *ppFileList* wurde ein fehlerhafter Zeiger übergeben.<br/>  |



 

## <a name="remarks"></a>Hinweise

Eine Liste aller von dieser Schnittstelle definierten Methoden finden Sie unter [**ISCardFileAccess**](iscardfileaccess.md).

Zusätzlich zu den oben aufgeführten COM-Fehlercodes gibt diese Schnittstelle möglicherweise einen Smartcardfehlercode zurück, wenn eine Smartcardfunktion aufgerufen wurde, um die Anforderung zu erfüllen. Weitere Informationen finden Sie unter [Smartcard-Rückgabewerte.](authentication-return-values.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ XP-Desktop-Apps\]<br/>          |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/> |
| Ende des Supports (Client)<br/>    | Windows XP<br/>                                |
| Ende des Supports (Server)<br/>    | Windows Server 2003<br/>                       |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**ISCardFileAccess**](iscardfileaccess.md)
</dt> </dl>

 

 
