---
description: Gibt an, ob das numerische Kennwort den speziellen Formatierungs Anforderungen für diesen Authentifizierungs Wert entspricht.
ms.assetid: 3995405f-db4d-4f72-98dc-133a09f9cf65
title: Isnumericalpasswordvalid-Methode der Win32_EncryptableVolume-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.IsNumericalPasswordValid
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 7cec4aa31ae9ff6aee90c0f46ded935b3d553783
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349548"
---
# <a name="isnumericalpasswordvalid-method-of-the-win32_encryptablevolume-class"></a>Isnumericalpasswordvalid-Methode der Win32- \_ Klasse "verschlüsseltablevolume"

Die **isnumericalpasswordvalid-** Methode der Win32-Klasse " [**\_ verschlüsseltablevolume**](win32-encryptablevolume.md) " gibt an, ob das numerische Kennwort die speziellen Formatierungs Anforderungen für diesen Authentifizierungs Wert erfüllt.

## <a name="syntax"></a>Syntax


```mof
uint32 IsNumericalPasswordValid(
  [in]  string  NumericalPassword,
  [out] boolean IsNumericalPasswordValid
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Numericalpassword* \[ in\]
</dt> <dd>

Typ: **Zeichenfolge**

Eine Zeichenfolge, die das numerische Kennwort angibt.

Das numerische Kennwort muss 48 Ziffern enthalten. Diese Ziffern können in 8 Gruppen mit 6 Ziffern aufgeteilt werden, wobei die letzte Ziffer in jeder Gruppe einen Prüfsummen Wert für die Gruppe angibt. Jede Gruppe von 6 Ziffern muss von 11 teilbar sein und muss kleiner als 720896 sein. Wenn eine Gruppe von sechs Ziffern als x1, x2, X3, X4, x5 und x6 bezeichnet wird, wird die Ziffer "Prüfsumme x6" als "– x1 + x2 – X3 + X4 – x5 mod 11" berechnet.

Die Gruppen von Ziffern können optional durch ein Leerzeichen oder einen Bindestrich getrennt werden. "Xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx" oder "xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx" kann daher auch gültige numerische Kenn Wörter enthalten.

</dd> <dt>

*Isnumericalpasswordvalid* \[ vorgenommen\]
</dt> <dd>

Typ: **booleschen**

Ein boolescher Wert, der true ist, wenn das numerische Kennwort den speziellen Formatanforderungen für diesen Authentifizierungs Wert entspricht; andernfalls ist der Wert false.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **UInt32**

Diese Methode gibt einen der folgenden Codes oder einen anderen Fehlercode zurück, wenn ein Fehler auftritt.



| Rückgabecode/-wert                                                                                                                                 | BESCHREIBUNG                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl> | Die Methode war erfolgreich.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen. MOF-Dateien werden nicht als Teil des Windows SDK installiert. Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista Enterprise, Windows Vista Ultimate \[ Desktop-Apps\]<br/>                       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                                    |
| Namespace<br/>                | Root \\ CIMV2 \\ Sicherheit ( \\ microsoftvolumeencryption)<br/>                                             |
| MOF<br/>                      | <dl> <dt>Win32 \_ verschlüsseltablevolume. MOF</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32- \_ verschlüsseltablevolume**](win32-encryptablevolume.md)
</dt> </dl>

 

 
