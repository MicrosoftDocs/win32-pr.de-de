---
title: EnvironmentVariables-Methode der Win32_TSExpandEnvironmentVariables Klasse
description: Erweitert systemdefinierte Umgebungsvariablen. | EnvironmentVariables-Methode der Win32_TSExpandEnvironmentVariables Klasse
ms.assetid: eff0dcdf-ef98-4730-9b0c-4f44250a607b
ms.tgt_platform: multiple
keywords:
- EnvironmentVariables-Remotedesktopdienste
- EnvironmentVariables-Methode Remotedesktopdienste , Win32_TSExpandEnvironmentVariables-Klasse
- Win32_TSExpandEnvironmentVariables klasse Remotedesktopdienste , EnvironmentVariables-Methode
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
ms.openlocfilehash: 49416291293d621739ab7c721ca349f5d87bb4582d1289f431a8c443d3414da1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118353892"
---
# <a name="environmentvariables-method-of-the-win32_tsexpandenvironmentvariables-class"></a>EnvironmentVariables-Methode der Win32 \_ TSExpandEnvironmentVariables-Klasse

Erweitert systemdefinierte Umgebungsvariablen.

## <a name="syntax"></a>Syntax


```mof
uint32 EnvironmentVariables(
  [in]  string OriginalString,
  [out] string ExpandedString
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*OriginalString* \[ In\]
</dt> <dd>

Eine Zeichenfolge, die die zu erweiternden Umgebungsvariablen enthält.

</dd> <dt>

*ExpandedString* \[ out\]
</dt> <dd>

Eine Zeichenfolge mit erweiterten Umgebungsvariablen.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Sie müssen Mitglied der Gruppe Administratoren sein, um diese Methode aufrufen zu können.

Managed Object Format -Dateien (MOF) enthalten die Definitionen für Windows WMI-Klassen (Management Instrumentation). MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert. Sie werden auf dem Server installiert, wenn Sie die zugeordnete Rolle mithilfe der Server-Manager. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | \\ \\ CiMv2-Stammterminaldienste<br/>                                                |
| MOF<br/>                      | <dl> <dt>Tsallow.mof</dt> </dl>  |
| DLL<br/>                      | <dl> <dt>TsPubWmi.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Win32 \_ TSExpandEnvironmentVariables**](win32-tsexpandenvironmentvariables.md)
</dt> </dl>

 

