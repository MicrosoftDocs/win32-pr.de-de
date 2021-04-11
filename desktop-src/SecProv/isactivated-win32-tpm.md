---
description: Die isaktivierte Methode der Win32- \_ TPM-Klasse gibt an, ob das Gerät aktiviert ist.
ms.assetid: 862c386c-c5b5-44d2-89a5-3735b99bf8bc
title: Isaktivierte Methode der Win32_Tpm-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.IsActivated
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 6482163a27f211b4f4ce24284a8339f2b7254f3a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217424"
---
# <a name="isactivated-method-of-the-win32_tpm-class"></a>Isaktivierte Methode der Win32- \_ TPM-Klasse

Die **isaktivierte** Methode der [**Win32- \_ TPM**](win32-tpm.md) -Klasse gibt an, ob das Gerät aktiviert ist.

## <a name="syntax"></a>Syntax


```mof
uint32 IsActivated(
  [out] boolean IsActivated
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Isaktiviert* \[ vorgenommen\]
</dt> <dd>

Typ: **booleschen**

**True** gibt an, dass das Gerät aktiviert ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **UInt32**

Alle TPM-Fehler sowie Fehler, die für die TPM-Basisdienste spezifisch sind, können zurückgegeben werden.

Allgemeine Rückgabecodes sind unten aufgeführt.



| Rückgabecode/-wert                                                                                                                                 | BESCHREIBUNG                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl> | Die Methode war erfolgreich.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Die Deaktivierung ist ähnlich wie bei deaktiviertem, aber Betriebsstatus Änderungen sind möglich. Gemäß der Trusted Computing Group (TCG) v 1.2-Spezifikation sind nur die folgenden Befehle verfügbar, wenn sich das Gerät in einem deaktivierten Zustand befindet.

-   TPM \_ continueselftest
-   TPM- \_ DSAP
-   TPM \_ flushspecific
-   TPM- \_ getcapability
-   TPM \_ gettestresult
-   TPM- \_ Init
-   TPM- \_ OIAP
-   TPM- \_ OSAP
-   TPM-Besitzer \_ setdeaktivierung
-   TPM- \_ PCR- \_ zurück Setzung
-   TPM- \_ physicaldeaktivieren
-   TPM- \_ physicalenable
-   TPM \_ physicalsetdeaktiviert
-   TPM- \_ zurück Setzung
-   TPM- \_ SaveState
-   TPM \_ selftestfull
-   TPM- \_ setcapability
-   TPM \_ SHA1Complete
-   TPM \_ SHA1Start
-   TPM \_ SHA1Update
-   TPM- \_ Start
-   TPM- \_ Besitz
-   TPM-Beendigungs \_ \_ handle

Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen. MOF-Dateien werden nicht als Teil des Windows SDK installiert. Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                      |
| Namespace<br/>                | Root \\ CIMV2 \\ Security- \\ mikrosofttpm<br/>                                            |
| MOF<br/>                      | <dl> <dt>Win32- \_ TPM. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Win32- \_tpm.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32- \_ TPM**](win32-tpm.md)
</dt> </dl>

 

 
