---
title: FileExtensions-Methode der Win32_TSApplicationFileExtensions-Klasse
description: Stellt eine Liste der Dateinamen Erweiterungen bereit, die von einer Anwendung behandelt werden.
ms.assetid: 833a1b68-86ed-4361-bbcb-a8d1c4a9306d
ms.tgt_platform: multiple
keywords:
- FileExtensions-Methode Remotedesktopdienste
- File Extensions-Methode Remotedesktopdienste, Win32_TSApplicationFileExtensions-Klasse
- Win32_TSApplicationFileExtensions-Klasse Remotedesktopdienste, FileExtensions-Methode
topic_type:
- apiref
api_name:
- Win32_TSApplicationFileExtensions.FileExtensions
api_location:
- TsPubWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5aa0bff92cdc274c8dba56aa11a44791e3ad9f01
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957066"
---
# <a name="fileextensions-method-of-the-win32_tsapplicationfileextensions-class"></a>FileExtensions-Methode der Win32- \_ Klasse "tyapplicationfileextensions"

Stellt eine Liste der Dateinamen Erweiterungen bereit, die von einer Anwendung behandelt werden.

## <a name="syntax"></a>Syntax


```mof
uint32 FileExtensions(
  [in]  string AppPath,
  [out] string Extensions[]
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Apppath* \[ in\]
</dt> <dd>

Pfad der Anwendung.

</dd> <dt>

*Erweiterungen* \[ vorgenommen\]
</dt> <dd>

Die Dateinamen Erweiterungen, die von der Anwendung behandelt werden.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Sie müssen Mitglied der Gruppe "Administratoren" sein, um diese Methode aufzurufen.

Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen. MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert. Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | Root \\ CIMv2 \\ TerminalServices<br/>                                                |
| MOF<br/>                      | <dl> <dt>Tsallow. MOF</dt> </dl>  |
| DLL<br/>                      | <dl> <dt>TsPubWmi.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32- \_ applicationfileextensions**](win32-tsapplicationfileextensions.md)
</dt> </dl>

 

