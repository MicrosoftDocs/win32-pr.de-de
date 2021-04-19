---
description: Ruft die virtuellen Flags für den angegebenen geöffneten Registrierungsschlüssel in einer Offline Registrierungs Struktur ab.
ms.assetid: 2a04c257-e3b0-415b-97d2-616e12513a0a
title: Orgetvirtualflags-Funktion (offreg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ORGetVirtualFlags
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: 36c41bb9e510a107689790162e03e3bb86c8de1b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370175"
---
# <a name="orgetvirtualflags-function"></a>Orgetvirtualflags-Funktion

Ruft die virtuellen Flags für den angegebenen geöffneten Registrierungsschlüssel in einer Offline Registrierungs Struktur ab.

## <a name="syntax"></a>Syntax


```C++
DWORD ORGetVirtualFlags(
  _In_  ORHKEY Handle,
  _Out_ PDWORD pdwFlags
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Handle* \[ in\]
</dt> <dd>

Ein Handle für einen geöffneten Registrierungsschlüssel in einer Offline Registrierungs Struktur.

</dd> <dt>

*pdwflags* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf eine Variable, die die für den Schlüssel festgelegten virtualisierungsflags empfängt. Nachdem die Funktion zurückgegeben wurde, kann dieser Parameter einen oder mehrere der folgenden Werte aufweisen.



| Wert                                                                                                                                                                                                                                                    | Bedeutung                                                                                                                                                                                                                                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="REG_KEY_DONT_SILENT_FAIL"></span><span id="reg_key_dont_silent_fail"></span><dl> <dt>**Reg \_ Schlüssel \_ \_ \_ nicht**</dt> unbeaufsichtigt Fehler <dt>4</dt> </dl> | Wenn dieses Flag festgelegt ist und ein Öffnungsvorgang für einen Schlüssel mit aktivierter Virtualisierung fehlschlägt, versucht die Registrierung nicht, den Schlüssel erneut zu öffnen. Wenn dieses Flag eindeutig ist, versucht die Registrierung, den Schlüssel mit dem maximal \_ zulässigen Zugriff erneut zu öffnen.<br/>                                                                                            |
| <span id="REG_KEY_DONT_VIRTUALIZE"></span><span id="reg_key_dont_virtualize"></span><dl> <dt>**Reg \_ Schlüssel \_ nicht \_ virtualisieren**</dt> <dt>2</dt> </dl>     | Wenn dieses Flag festgelegt ist und ein Create Key-Vorgang fehlschlägt, da der Aufrufer nicht über den Key \_ Create \_ Sub Key-Schlüssel \_ für den übergeordneten Schlüssel verfügt, schlägt die Registrierung den Erstellungs Vorgang fehl. Wenn dieses Flag eindeutig ist, versucht die Registrierung, den Schlüssel im virtuellen Speicher zu erstellen. Der Aufrufer muss über die Berechtigung zum Lesen des Schlüssels \_ für den übergeordneten Schlüssel verfügen.<br/> |
| <span id="REG_KEY_RECURSE_FLAG"></span><span id="reg_key_recurse_flag"></span><dl> <dt>**Reg \_ Key \_ recurse- \_ Flag**</dt> <dt>8</dt> </dl>              | Wenn dieses Flag festgelegt ist, werden registrierungsvirtualisierungsflags aus dem übergeordneten Schlüssel weitergegeben. Wenn dieses Flag eindeutig ist, werden die registrierungsvirtualisierungsflags nicht weitergegeben.<br/>                                                                                                                                                                    |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert Fehler \_ erfolgreich.

Wenn die Funktion fehlschlägt, ist der Rückgabewert ein Fehlercode ungleich 0 (null), der in WinError. h definiert ist. Sie können die [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) -Funktion mit dem \_ Flag Format Message \_ from System verwenden \_ , um eine generische Beschreibung des Fehlers zu erhalten.

## <a name="remarks"></a>Bemerkungen

Die Registrierungsvirtualisierung ist eine zwischen Anwendungskompatibilitäts-Technologie, die es ermöglicht, Registrierungs Schreibvorgänge mit globaler Auswirkung an benutzerspezifische Speicherorte umzuleiten. Diese Umleitung ist für Anwendungen transparent, die aus der Registrierung lesen oder in diese schreiben.

Die Registrierungsvirtualisierung wird ab Windows Vista unterstützt. Microsoft beabsichtigt jedoch, Sie aus zukünftigen Versionen des Windows-Betriebssystems zu entfernen, da mehr Anwendungen mit Windows Vista kompatibel gemacht werden. Daher sollten Anwendungen nicht vom Verhalten der Registrierungsvirtualisierung im System abhängen.

Die Registrierungsvirtualisierung ist nur für Folgendes aktiviert:

-   interaktive 32-Bit-Prozesse
-   Schlüssel in **HKEY \_ - \_ \\ Software für lokale Computer**
-   Schlüssel, in die ein Administrator schreiben kann

Weitere Informationen finden Sie unter [Registrierungsvirtualisierung](../sysinfo/registry-virtualization.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|---------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | Windows-offline Registrierungs Bibliothek, Version 1,0 oder höher<br/>                      |
| Header<br/>          | <dl> <dt>Offreg. h</dt> </dl>   |
| DLL<br/>             | <dl> <dt>Offreg.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Orsetvirtualflags**](orsetvirtualflags.md)
</dt> <dt>

[Registrierungsvirtualisierung](../sysinfo/registry-virtualization.md)
</dt> </dl>

 

 
