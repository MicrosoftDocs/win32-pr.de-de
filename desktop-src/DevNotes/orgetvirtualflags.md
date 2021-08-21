---
description: Ruft die virtuellen Flags für den angegebenen geöffneten Registrierungsschlüssel in einer Offlineregistrierungsstruktur ab.
ms.assetid: 2a04c257-e3b0-415b-97d2-616e12513a0a
title: ORGetVirtualFlags-Funktion (Offreg.h)
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
ms.openlocfilehash: 8f0e44c388b576bb514ed86f2a537cefaf1a4f0984e3e5beb1b466e88c5b82c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119076054"
---
# <a name="orgetvirtualflags-function"></a>ORGetVirtualFlags-Funktion

Ruft die virtuellen Flags für den angegebenen geöffneten Registrierungsschlüssel in einer Offlineregistrierungsstruktur ab.

## <a name="syntax"></a>Syntax


```C++
DWORD ORGetVirtualFlags(
  _In_  ORHKEY Handle,
  _Out_ PDWORD pdwFlags
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Handle* \[ In\]
</dt> <dd>

Ein Handle für einen geöffneten Registrierungsschlüssel in einer Offlineregistrierungsstruktur.

</dd> <dt>

*pdwFlags* \[ out\]
</dt> <dd>

Ein Zeiger auf eine Variable, um die für den Schlüssel festgelegten Virtualisierungsflags zu empfangen. Nachdem die Funktion zurückgegeben wurde, kann dieser Parameter mindestens einen der folgenden Werte aufweisen.



| Wert                                                                                                                                                                                                                                                    | Bedeutung                                                                                                                                                                                                                                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="REG_KEY_DONT_SILENT_FAIL"></span><span id="reg_key_dont_silent_fail"></span><dl> <dt>**REG \_ KEY \_ DONT \_ SILENT \_ FAIL**</dt> <dt>4</dt> </dl> | Wenn dieses Flag festgelegt ist und bei einem Schlüssel mit aktivierter Virtualisierung ein Open-Vorgang fehlschlägt, versucht die Registrierung nicht, den Schlüssel erneut zu öffnen. Wenn dieses Flag eindeutig ist, versucht die Registrierung, den Schlüssel mit maximal zulässigem Zugriff erneut zu \_ öffnen.<br/>                                                                                            |
| <span id="REG_KEY_DONT_VIRTUALIZE"></span><span id="reg_key_dont_virtualize"></span><dl> <dt>**REG \_ KEY \_ DONT \_ VIRTUALIZE**</dt> <dt>2</dt> </dl>     | Wenn dieses Flag festgelegt ist und ein Vorgang zum Erstellen eines Schlüssels fehlschlägt, weil der Aufrufer nicht über die Berechtigung KEY \_ CREATE SUB KEY für den \_ \_ übergeordneten Schlüssel verfügt, schlägt die Registrierung den Erstellungsvorgang fehl. Wenn dieses Flag eindeutig ist, versucht die Registrierung, den Schlüssel im virtuellen Speicher zu erstellen. Der Aufrufer muss über die BERECHTIGUNG KEY \_ READ für den übergeordneten Schlüssel verfügen.<br/> |
| <span id="REG_KEY_RECURSE_FLAG"></span><span id="reg_key_recurse_flag"></span><dl> <dt>**REG \_ KEY \_ RECURSE \_ FLAG**</dt> <dt>8</dt> </dl>              | Wenn dieses Flag festgelegt ist, werden Registrierungsvirtualisierungsflags vom übergeordneten Schlüssel weitergegeben. Wenn dieses Flag eindeutig ist, werden Registrierungsvirtualisierungsflags nicht weitergegeben.<br/>                                                                                                                                                                    |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, lautet der Rückgabewert ERROR \_ SUCCESS.

Wenn die Funktion fehlschlägt, ist der Rückgabewert ein Fehlercode ungleich 0 (null), der in Winerror.h definiert ist. Sie können die [FormatMessage-Funktion](/windows/win32/api/winbase/nf-winbase-formatmessage) mit dem \_ FORMAT MESSAGE FROM \_ \_ SYSTEM-Flag verwenden, um eine generische Beschreibung des Fehlers abzurufen.

## <a name="remarks"></a>Hinweise

Die Registrierungsvirtualisierung ist eine Zwischenanwendungskompatibilitätstechnologie, mit der Schreibvorgänge für Registrierungen, die globale Auswirkungen haben, an benutzerspezifische Speicherorte umgeleitet werden können. Diese Umleitung ist für Anwendungen transparent, die aus der Registrierung lesen oder in die Registrierung schreiben.

Die Registrierungsvirtualisierung wird ab Windows Vista unterstützt. Microsoft beabsichtigt jedoch, es aus zukünftigen Versionen des Windows Betriebssystems zu entfernen, da mehr Anwendungen mit Windows Vista kompatibel gemacht werden. Daher sollten Anwendungen nicht vom Verhalten der Registrierungsvirtualisierung im System abhängen.

Die Registrierungsvirtualisierung ist nur für Folgendes aktiviert:

-   Interaktive 32-Bit-Prozesse
-   Schlüssel in **HKEY \_ LOCAL MACHINE \_ \\ Software**
-   Schlüssel, in die ein Administrator schreiben kann

Weitere Informationen finden Sie unter [Registry Virtualization](../sysinfo/registry-virtualization.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|---------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | Windows Offline registry library version 1.0 or later (Offlineregistrierungsbibliothek, Version 1.0 oder höher)<br/>                      |
| Header<br/>          | <dl> <dt>Offreg.h</dt> </dl>   |
| DLL<br/>             | <dl> <dt>Offreg.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ORSetVirtualFlags**](orsetvirtualflags.md)
</dt> <dt>

[Registrierungsvirtualisierung](../sysinfo/registry-virtualization.md)
</dt> </dl>

 

 
