---
description: Schreibt die angegebene Offline Registrierungs Struktur in eine Datei.
ms.assetid: 26f2eed9-e6e0-4dc0-8b91-212cde072744
title: Orsavehive-Funktion (offreg. h)
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
ms.openlocfilehash: 59df5b191a9bc0cfe98e1681665c5814935aa2c3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370564"
---
# <a name="orsavehive-function"></a>Orsavehive-Funktion

Schreibt die angegebene Offline Registrierungs Struktur in eine Datei.

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

*Handle* \[ in\]
</dt> <dd>

Ein Handle für die zu speichernde Offline Registrierungs Struktur.

</dd> <dt>

*lphivepath* \[ in\]
</dt> <dd>

Ein Zeiger auf eine Unicode-Zeichenfolge, die den Namen der Hive-Registrierungsdatei angibt. Dabei kann es sich nicht um den Namen einer vorhandenen Datei handeln.

</dd> <dt>

*dwOSMajorVersion* \[ in\]
</dt> <dd>

Die Hauptversionsnummer des Betriebssystems. Dieser Member kann einen der folgenden Werte aufweisen.



| Wert                                                                        | Bedeutung                                                                                                                                                                                                                        |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>5</dt> </dl> | Wenn *dwOSMinorVersion* den Wert 1 hat, ist das Betriebssystem Windows XP.<br/> Wenn *dwOSMinorVersion* 2 ist, ist das Betriebssystem Windows Server 2003 R2, Windows Server 2003 oder Windows XP Professional x64 Edition.<br/> |
| <dl> <dt>6</dt> </dl> | Wenn *dwOSMinorVersion* den Wert 0 hat, ist das Betriebssystem Windows Server 2008 oder Windows Vista.<br/> Wenn *dwOSMinorVersion* den Wert 1 hat, ist das Betriebssystem Windows Server 2008 R2 oder Windows 7.<br/>                       |



 

</dd> <dt>

*dwOSMinorVersion* \[ in\]
</dt> <dd>

Die neben Versionsnummer des Betriebssystems. Dieser Member kann einen der folgenden Werte aufweisen.



| Wert                                                                        | Bedeutung                                                                                                                                                                                                                                       |
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl> | Wenn *dwOSMajorVersion* den Wert 6 hat, ist das Betriebssystem Windows Server 2008 oder Windows Vista.<br/>                                                                                                                                          |
| <dl> <dt>1</dt> </dl> | Wenn *dwOSMajorVersion* den Wert 5 hat, ist das Betriebssystem Windows XP.<br/> Wenn *dwOSMajorVersion* den Wert 6 hat, ist das Betriebssystem Windows Server 2008 R2 oder Windows 7.<br/>                                                                |
| <dl> <dt>2</dt> </dl> | Wenn *dwOSMajorVersion* den Wert 5 hat, ist das Betriebssystem Windows Server 2003 R2, Windows Server 2003 oder Windows XP Professional x64 Edition. <br/> Wenn *dwOSMajorVersion* den Wert 6 hat, muss der *dwOSMinorVersion* -Parameter den Wert 0 oder 1 aufweisen. <br/> |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert Fehler \_ erfolgreich.

Wenn die Funktion fehlschlägt, ist der Rückgabewert ein Fehlercode ungleich 0 (null), der in WinError. h definiert ist. Sie können die [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) -Funktion mit dem \_ Flag Format Message \_ from System verwenden \_ , um eine generische Beschreibung des Fehlers zu erhalten. Folgende Fehlercodes sind möglich:

-   Wenn der Aufrufer nicht über die erforderlichen Zugriffsrechte zum Schreiben der Datei verfügt, gibt die Funktion den Fehler \_ Zugriff \_ verweigert zurück.
-   Wenn die angegebene Datei bereits vorhanden ist, gibt die Funktion einen Fehler zurück \_ \_ .

## <a name="remarks"></a>Bemerkungen

Die **orsavehive** -Funktion muss verwendet werden, um an einer Offline Registrierungs Struktur vorgenommene Änderungen zu speichern. Änderungen werden nicht beibehalten, bis **orsavehive** aufgerufen wird, um die Struktur in einer Datei zu speichern.

Die Parameter *dwOSMajorVersion* und *dwOSMinorVersion* geben das Zielformat der Hive-Registrierungsdatei an. In der folgenden Tabelle werden die aktuellen Versionsnummern des Betriebssystems zusammengefasst.



| Betriebssystem                    | Versionsnummer |
|-------------------------------------|----------------|
| Windows Server 2008 R2              | 6.1            |
| Windows 7                           | 6.1            |
| Windows Server 2008                 | 6.0            |
| Windows Vista                       | 6.0            |
| Windows Server 2003 R2              | 5,2            |
| Windows Server 2003                 | 5,2            |
| Windows XP Professional x64 Edition | 5,2            |
| Windows XP                          | 5,1            |



 

Verwenden Sie die Funktion [GetVersionEx](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getversionexa) zum Abrufen von Informationen zum aktuellen Betriebssystem.

Die **orsavehive** -Funktion sperrt die Registrierungs Struktur, während Sie die Struktur in die Datei schreibt, schließt dann die Datei und gibt die Sperre frei. Die Registrierungs Struktur verbleibt im Arbeitsspeicher, bis Sie durch Aufrufen der [**orclosehive**](orclosehive.md) -Funktion geschlossen wird. Es ist möglich, Änderungen an der Registrierungs Struktur vorzunehmen, während Sie geöffnet ist. um diese Änderungen beizubehalten, muss die Struktur jedoch in einer neuen Datei gespeichert werden, da die **orsavehive** -Funktion eine vorhandene Datei nicht überschreibt.

Die **orsavehive** -Funktion kann verwendet werden, um einen Teil der Offline Registrierungs Struktur zu speichern. Der im *handle* -Parameter angegebene Schlüssel wird zum Stamm Schlüssel einer Struktur, die aus dem angegebenen Schlüssel und den zugehörigen unter Schlüsseln besteht.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|---------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | Windows-offline Registrierungs Bibliothek, Version 1,0 oder höher<br/>                      |
| Header<br/>          | <dl> <dt>Offreg. h</dt> </dl>   |
| DLL<br/>             | <dl> <dt>Offreg.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[GetVersionEx](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getversionexa)
</dt> <dt>

[**Orclosehive**](orclosehive.md)
</dt> <dt>

[**Oropenhive**](oropenhive.md)
</dt> </dl>

 

 
