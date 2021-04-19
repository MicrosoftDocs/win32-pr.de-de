---
title: Umgebungs variables-Methode der Win32_TSExpandEnvironmentVariables-Klasse
description: Erweitert System definierte Umgebungsvariablen. | Umgebungs variables-Methode der Win32_TSExpandEnvironmentVariables-Klasse
ms.assetid: eff0dcdf-ef98-4730-9b0c-4f44250a607b
ms.tgt_platform: multiple
keywords:
- Umgebungs variables-Methode Remotedesktopdienste
- Umgebungs variables-Methode Remotedesktopdienste, Win32_TSExpandEnvironmentVariables-Klasse
- Win32_TSExpandEnvironmentVariables-Klasse Remotedesktopdienste, Umgebungs variables-Methode
topic_type:
- apiref
api_name:
- Win32_TSExpandEnvironmentVariables.EnvironmentVariables
api_location:
- TsPubWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6f038ee1d5f93c11336657f9b8c1a80ecc05d6d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106355129"
---
# <a name="environmentvariables-method-of-the-win32_tsexpandenvironmentvariables-class"></a>Umgebungs variables-Methode der Win32- \_ Klasse "tsexpandumgebungsvariables"

Erweitert System definierte Umgebungsvariablen.

## <a name="syntax"></a>Syntax


```mof
uint32 EnvironmentVariables(
  [in]  string OriginalString,
  [out] string ExpandedString
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*OriginalString* \[ in\]
</dt> <dd>

Eine Zeichenfolge, die die Umgebungsvariablen enthält, die erweitert werden sollen.

</dd> <dt>

*Expandecodstring* \[ vorgenommen\]
</dt> <dd>

Eine Zeichenfolge, in der die Umgebungsvariablen erweitert werden.

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

[**Win32 \_ tsexpandumgebungs variables**](win32-tsexpandenvironmentvariables.md)
</dt> </dl>

 

