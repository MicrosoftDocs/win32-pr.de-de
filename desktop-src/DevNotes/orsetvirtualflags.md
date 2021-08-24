---
description: Legt Virtualisierungsflags für den angegebenen offenen Registrierungsschlüssel in einer Offlineregistrierungsstruktur fest.
ms.assetid: c625af35-8e14-4379-8d0a-6f5b65a1aebb
title: ORSetVirtualFlags-Funktion (Offreg.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ORSetVirtualFlags
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: 56ca40b273447c8669c162b8c2dba597f2b2ce98282d40e7b482d04032a5f95a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119815440"
---
# <a name="orsetvirtualflags-function"></a>ORSetVirtualFlags-Funktion

Legt Virtualisierungsflags für den angegebenen offenen Registrierungsschlüssel in einer Offlineregistrierungsstruktur fest.

## <a name="syntax"></a>Syntax


```C++
DWORD ORSetVirtualFlags(
  _In_ ORHKEY Handle,
  _In_ DWORD  dwFlags
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Handle* \[ In\]
</dt> <dd>

Ein Handle für einen geöffneten Registrierungsschlüssel in einer Offlineregistrierungsstruktur.

</dd> <dt>

*dwFlags* \[ In\]
</dt> <dd>

Dieser Parameter steuert das Verhalten der Registrierung, wenn ein Create- oder Open-Vorgang für einen Schlüssel in einer virtualisierten Struktur fehlschlägt. Dieser Parameter kann einen oder mehrere der folgenden Werte sein.



| Wert                                                                                                                                                                                                                                                    | Bedeutung                                                                                                                                                                                                                                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="REG_KEY_DONT_SILENT_FAIL"></span><span id="reg_key_dont_silent_fail"></span><dl> <dt>**REG \_ KEY \_ DONT \_ SILENT \_ FAIL**</dt> <dt>4</dt> </dl> | Wenn dieses Flag festgelegt ist und ein Open-Vorgang für einen Schlüssel fehlschlägt, für den die Virtualisierung aktiviert ist, versucht die Registrierung nicht, den Schlüssel erneut zu öffnen. Wenn dieses Flag eindeutig ist, versucht die Registrierung, den Schlüssel mit dem Zugriff MAXIMUM \_ ALLOWED erneut zu öffnen.<br/>                                                                                    |
| <span id="REG_KEY_DONT_VIRTUALIZE"></span><span id="reg_key_dont_virtualize"></span><dl> <dt>**REG \_ KEY \_ DONT \_ VIRTUALIZE**</dt> <dt>2</dt> </dl>     | Wenn dieses Flag festgelegt ist und bei einem Vorgang zum Erstellen eines Schlüssels ein Fehler auftritt, weil der Aufrufer nicht über den SCHLÜSSEL CREATE SUB KEY für den übergeordneten Schlüssel verfügt, schlägt die Registrierung mit dem \_ \_ \_ Erstellungsvorgang fehl. Wenn dieses Flag eindeutig ist, versucht die Registrierung, den Schlüssel im virtuellen Speicher zu erstellen. Der Aufrufer muss über das Recht KEY \_ READ für den übergeordneten Schlüssel verfügen.<br/> |
| <span id="REG_KEY_RECURSE_FLAG"></span><span id="reg_key_recurse_flag"></span><dl> <dt>**REG \_ KEY \_ RECURSE \_ FLAG**</dt> <dt>8</dt> </dl>              | Wenn dieses Flag festgelegt ist, werden Registrierungsvirtualisierungsflags vom übergeordneten Schlüssel propagiert. Wenn dieses Flag eindeutig ist, werden Registrierungsvirtualisierungsflags nicht propagiert.<br/>                                                                                                                                                                    |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, ist der Rückgabewert ERROR \_ SUCCESS.

Wenn die Funktion fehlschlägt, ist der Rückgabewert ein fehlerfreier Code, der in Winerror.h definiert ist. Sie können die [FormatMessage-Funktion](/windows/win32/api/winbase/nf-winbase-formatmessage) mit dem Flag FORMAT \_ MESSAGE FROM SYSTEM \_ \_ verwenden, um eine generische Beschreibung des Fehlers zu erhalten.

## <a name="remarks"></a>Hinweise

Die Registrierungsvirtualisierung ist eine Zwischentechnologie zur Anwendungskompatibilität, mit der Schreibvorgänge in Registrierungen, die globale Auswirkungen haben, an benutzerspezifische Speicherorte umgeleitet werden können. Diese Umleitung ist für Anwendungen transparent, die aus der Registrierung lesen oder in diese schreiben.

Die Registrierungsvirtualisierung wird ab Windows Vista unterstützt. Microsoft möchte es jedoch aus zukünftigen Versionen des Windows-Betriebssystems entfernen, da mehr Anwendungen mit Windows Vista kompatibel gemacht werden. Daher sollten Anwendungen nicht vom Verhalten der Registrierungsvirtualisierung im System abhängen.

Die Registrierungsvirtualisierung ist nur für Folgendes aktiviert:

-   Interaktive 32-Bit-Prozesse
-   Schlüssel in **HKEY \_ LOCAL MACHINE \_ \\ Software**
-   Schlüssel, in die ein Administrator schreiben kann

Weitere Informationen finden Sie unter [Registrierungsvirtualisierung.](../sysinfo/registry-virtualization.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|---------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | Windows Offlineregistrierungsbibliothek, Version 1.0 oder höher<br/>                      |
| Header<br/>          | <dl> <dt>Offreg.h</dt> </dl>   |
| DLL<br/>             | <dl> <dt>Offreg.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ORGetVirtualFlags**](orgetvirtualflags.md)
</dt> <dt>

[Registrierungsvirtualisierung](../sysinfo/registry-virtualization.md)
</dt> </dl>

 

 
