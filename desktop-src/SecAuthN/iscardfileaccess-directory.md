---
description: Die Directory-Methode ruft eine Liste der Dateien des angegebenen Typs aus dem aktuellen Verzeichnis ab.
ms.assetid: 0ae89811-7534-497b-af9f-ae37a48bc3e5
title: Iscardfileaccess::D irectory-Methode
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
ms.openlocfilehash: 74293d4fa97a61133739cac75f17eaffed6e52b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864048"
---
# <a name="iscardfileaccessdirectory-method"></a>Iscardfileaccess::D irectory-Methode

\[Die **Verzeichnis** Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die [Smartcard-Module](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten eine ähnliche Funktionalität.\]

Die **Directory** -Methode ruft eine Liste der Dateien des angegebenen Typs aus dem aktuellen Verzeichnis ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT Directory(
  [in]  FILETYPE    fileType,
  [out] LPSAFEARRAY *ppFileList
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*filetype* \[ in\]
</dt> <dd>

Typ der aufzulistenden [*smartcarddateien*](../secgloss/s-gly.md) .



| Wert                                                                                                                                                                                      | Bedeutung                                              |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <span id="SC_TYPE_DIRECTORIES"></span><span id="sc_type_directories"></span><dl> <dt>**SC \_ - \_ typverzeichnisse**</dt> </dl>           | Nur Verzeichnis Dateien auflisten.<br/>                |
| <span id="SC_TYPE_FILES"></span><span id="sc_type_files"></span><dl> <dt>**SC \_ - \_ Typdateien**</dt> </dl>                             | Nur elementare Dateien auflisten.<br/>               |
| <span id="SC_TYPE_ALL_FILES"></span><span id="sc_type_all_files"></span><dl> <dt>**SC \_ Geben Sie \_ alle \_ Dateien ein.**</dt> </dl>                | Auflisten von Verzeichnis-und elementaren Dateien<br/> |
| <span id="SC_TYPE_DIRECTORY_FILE"></span><span id="sc_type_directory_file"></span><dl> <dt>**SC \_ - \_ typverzeichnis \_ Datei**</dt> </dl> | Verzeichnis Datei.<br/>                           |
| <span id="SC_TYPE_TRANSPARENT_EF"></span><span id="sc_type_transparent_ef"></span><dl> <dt>**SC \_ Type \_ transparent \_ EF**</dt> </dl> | Transparente elementare Datei.<br/>              |
| <span id="SC_TYPE_FIXED_EF"></span><span id="sc_type_fixed_ef"></span><dl> <dt>**"SC \_ Type \_ Fixed \_ EF"**</dt> </dl>                   | Lineare, behobene elementare Datei.<br/>             |
| <span id="SC_TYPE_CYCLIC_EF"></span><span id="sc_type_cyclic_ef"></span><dl> <dt>**SC \_ Type \_ zyklische \_ EF**</dt> </dl>                | Zyklische elementare Datei.<br/>                   |
| <span id="SC_TYPE_VARIABLE_EF"></span><span id="sc_type_variable_ef"></span><dl> <dt>**SC \_ - \_ Typvariable \_ EF**</dt> </dl>          | Lineare Variable (elementare Datei).<br/>          |



 

</dd> <dt>

*ppfilelist* \[ vorgenommen\]
</dt> <dd>

Array von bstrins, das die Liste der Dateien darstellt, die mit dem Spezifizierer in *filetype* übereinstimmen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die-Methode gibt einen der folgenden möglichen Werte zurück.



| Rückgabecode                                                                                   | Beschreibung                                               |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Der Vorgang wurde erfolgreich abgeschlossen.<br/>          |
| <dl> <dt>**E \_ invalidArg**</dt> </dl>  | Ungültiger Parameter.<br/>                             |
| <dl> <dt>**E \_ notimpl**</dt> </dl>     | Diese Methode wurde von der-Schnittstelle nicht implementiert.<br/> |
| <dl> <dt>**E \_ outo-Memory**</dt> </dl> | Nicht genügend Arbeitsspeicher.<br/>                                 |
| <dl> <dt>**E- \_ Zeiger**</dt> </dl>     | Für *ppfilelist* wurde ein fehlerhafter Zeiger übermittelt.<br/>  |



 

## <a name="remarks"></a>Bemerkungen

Eine Liste aller Methoden, die durch diese Schnittstelle definiert werden, finden Sie unter [**iscardfileaccess**](iscardfileaccess.md).

Zusätzlich zu den oben aufgeführten com-Fehlercodes gibt diese Schnittstelle möglicherweise einen Fehlercode für die Smartcard zurück, wenn eine smartcardfunktion aufgerufen wurde, um die Anforderung abzuschließen. Weitere Informationen finden Sie unter [Smartcard-Rückgabewerte](authentication-return-values.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>          |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/> |
| Ende des Supports (Client)<br/>    | Windows XP<br/>                                |
| Ende des Supports (Server)<br/>    | Windows Server 2003<br/>                       |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iscardfileaccess**](iscardfileaccess.md)
</dt> </dl>

 

 
