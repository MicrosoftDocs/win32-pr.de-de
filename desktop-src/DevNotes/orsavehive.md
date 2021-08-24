---
description: Schreibt die angegebene Offlineregistrierungsstruktur in eine Datei.
ms.assetid: 26f2eed9-e6e0-4dc0-8b91-212cde072744
title: ORSaveHive-Funktion (Offreg.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ORSaveHive
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: 0b4dde44b6cc6d2c5cfd80f4041cd6370f680eb6ca867e9e8f2bbce5f0702e27
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119758510"
---
# <a name="orsavehive-function"></a>ORSaveHive-Funktion

Schreibt die angegebene Offlineregistrierungsstruktur in eine Datei.

## <a name="syntax"></a>Syntax


```C++
DWORD ORSaveHive(
  _In_ ORHKEY Handle,
  _In_ PCWSTR lpHivePath,
  _In_ DWORD  dwOsMajorVersion,
  _In_ DWORD  dwOsMinorVersion
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Handle* \[ In\]
</dt> <dd>

Ein Handle für die zu speichernde Offlineregistrierungsstruktur.

</dd> <dt>

*lpHivePath* \[ In\]
</dt> <dd>

Ein Zeiger auf eine Unicode-Zeichenfolge, die den Namen der Registrierungsstrukturdatei angibt. Dies darf nicht der Name einer vorhandenen Datei sein.

</dd> <dt>

*dwOsMajorVersion* \[ In\]
</dt> <dd>

Die Hauptversionsnummer des Betriebssystems. Dieser Member kann einer der folgenden Werte sein.



| Wert                                                                        | Bedeutung                                                                                                                                                                                                                        |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>5</dt> </dl> | Wenn *dwOsMinorVersion* 1 ist, wird das Windows XP verwendet.<br/> Wenn *dwOsMinorVersion* 2 ist, ist das Betriebssystem Windows Server 2003 R2, Windows Server 2003 oder Windows XP Professional x64 Edition.<br/> |
| <dl> <dt>6</dt> </dl> | Wenn *dwOsMinorVersion* 0 ist, wird das Betriebssystem Windows Server 2008 oder Windows Vista installiert.<br/> Wenn *dwOsMinorVersion* 1 ist, wird das Windows Server 2008 R2 oder Windows 7 verwendet.<br/>                       |



 

</dd> <dt>

*dwOsMinorVersion* \[ In\]
</dt> <dd>

Die Nebenversionsnummer des Betriebssystems. Dieser Member kann einer der folgenden Werte sein.



| Wert                                                                        | Bedeutung                                                                                                                                                                                                                                       |
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl> | Wenn *dwOsMajorVersion* 6 ist, wird das Betriebssystem Windows Server 2008 oder Windows Vista installiert.<br/>                                                                                                                                          |
| <dl> <dt>1</dt> </dl> | Wenn *dwOsMajorVersion* 5 ist, wird das Betriebssystem Windows XP verwendet.<br/> Wenn *dwOsMajorVersion* 6 ist, ist das Betriebssystem Windows Server 2008 R2 oder Windows 7.<br/>                                                                |
| <dl> <dt>2</dt> </dl> | Wenn *dwOsMajorVersion* 5 ist, ist das Betriebssystem Windows Server 2003 R2, Windows Server 2003 oder Windows XP Professional x64 Edition. <br/> Wenn *dwOsMajorVersion* 6 ist, muss *der dwOsMinorVersion-Parameter* 0 oder 1 sein. <br/> |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, ist der Rückgabewert ERROR \_ SUCCESS.

Wenn die Funktion fehlschlägt, ist der Rückgabewert ein fehlerfreier Code, der in Winerror.h definiert ist. Sie können die [FormatMessage-Funktion](/windows/win32/api/winbase/nf-winbase-formatmessage) mit dem Flag FORMAT \_ MESSAGE FROM SYSTEM \_ \_ verwenden, um eine generische Beschreibung des Fehlers zu erhalten. Mögliche Fehlercodes:

-   Wenn der Aufrufer nicht über die erforderlichen Zugriffsrechte zum Schreiben der Datei verfügt, gibt die Funktion ERROR \_ ACCESS \_ DENIED zurück.
-   Wenn die angegebene Datei bereits vorhanden ist, gibt die Funktion ERROR \_ ALREADY \_ EXISTS zurück.

## <a name="remarks"></a>Hinweise

Die **ORSaveHive-Funktion** muss verwendet werden, um Änderungen an einer Offlineregistrierungsstruktur zu speichern. Änderungen werden erst beibehalten, wenn **ORSaveHive aufgerufen** wird, um die Struktur in einer Datei zu speichern.

Die *Parameter dwOsMajorVersion* und *dwOsMinorVersion* geben zusammen das Zielformat der Registrierungsstrukturdatei an. In der folgenden Tabelle sind die neuesten Betriebssystemversionsnummern zusammengefasst.



| Betriebssystem                    | Versionsnummer |
|-------------------------------------|----------------|
| Windows Server 2008 R2              | 6.1            |
| Windows 7                           | 6.1            |
| Windows Server 2008                 | 6.0            |
| Windows Vista                       | 6.0            |
| Windows Server 2003 R2              | 5,2            |
| Windows Server 2003                 | 5,2            |
| Windows XP Professional x64 Edition | 5,2            |
| Windows XP                          | 5,1            |



 

Verwenden Sie [die GetVersionEx-Funktion,](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getversionexa) um Informationen zum aktuellen Betriebssystem abzurufen.

Die **ORSaveHive-Funktion** sperrt die Registrierungsstruktur, während sie die Struktur in die Datei schreibt, schließt dann die Datei und gibt die Sperre frei. Die Registrierungsstruktur verbleibt im Arbeitsspeicher, bis sie durch Aufrufen der [**ORCloseHive-Funktion geschlossen**](orclosehive.md) wird. Es ist möglich, weitere Änderungen an der Registrierungsstruktur vorzunehmen, während sie geöffnet ist. Um diese Änderungen zu erhalten, muss die Struktur jedoch in einer neuen Datei gespeichert werden, da die **ORSaveHive-Funktion** keine vorhandene Datei überschreibt.

Die **ORSaveHive-Funktion** kann verwendet werden, um einen Teil der Offlineregistrierungsstruktur zu speichern. Der im *Handle-Parameter* angegebene Schlüssel wird zum Stammschlüssel einer Struktur, die aus dem angegebenen Schlüssel und allen unteren Schlüsseln besteht.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|---------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | Windows Offlineregistrierungsbibliothek, Version 1.0 oder höher<br/>                      |
| Header<br/>          | <dl> <dt>Offreg.h</dt> </dl>   |
| DLL<br/>             | <dl> <dt>Offreg.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Getversionex](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getversionexa)
</dt> <dt>

[**ORCloseHive**](orclosehive.md)
</dt> <dt>

[**OROpenHive**](oropenhive.md)
</dt> </dl>

 

 
