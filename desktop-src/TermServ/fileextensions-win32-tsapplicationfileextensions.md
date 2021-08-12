---
title: FileExtensions-Methode der Win32_TSApplicationFileExtensions-Klasse
description: Stellt eine Liste der Dateinamenerweiterungen bereit, die von einer Anwendung behandelt werden.
ms.assetid: 833a1b68-86ed-4361-bbcb-a8d1c4a9306d
ms.tgt_platform: multiple
keywords:
- FileExtensions-Methode Remotedesktopdienste
- FileExtensions-Methode Remotedesktopdienste , Win32_TSApplicationFileExtensions-Klasse
- Win32_TSApplicationFileExtensions Klasse Remotedesktopdienste , FileExtensions-Methode
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
ms.openlocfilehash: a3c7c44acd410566c4f048cdf36bac904c18b21df42f53543051e3b94f49bfbb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118609372"
---
# <a name="fileextensions-method-of-the-win32_tsapplicationfileextensions-class"></a>FileExtensions-Methode der Win32 \_ TSApplicationFileExtensions-Klasse

Stellt eine Liste der Dateinamenerweiterungen bereit, die von einer Anwendung behandelt werden.

## <a name="syntax"></a>Syntax


```mof
uint32 FileExtensions(
  [in]  string AppPath,
  [out] string Extensions[]
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*AppPath* \[ In\]
</dt> <dd>

Pfad der Anwendung.

</dd> <dt>

*Erweiterungen* \[ out\]
</dt> <dd>

Die Dateinamenerweiterungen, die von der Anwendung behandelt werden.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Sie müssen Mitglied der Gruppe Administratoren sein, um diese Methode aufzurufen.

Managed Object Format -Dateien (MOF) enthalten die Definitionen für Windows Management Instrumentation -Klassen (WMI). MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert. Sie werden auf dem Server installiert, wenn Sie die zugeordnete Rolle mithilfe der Server-Manager hinzufügen. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | Root \\ CIMv2 \\ TerminalServices<br/>                                                |
| MOF<br/>                      | <dl> <dt>Tsallow.mof</dt> </dl>  |
| DLL<br/>                      | <dl> <dt>TsPubWmi.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Win32 \_ TSApplicationFileExtensions**](win32-tsapplicationfileextensions.md)
</dt> </dl>

 

