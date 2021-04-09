---
title: Sisfrezupedmemory-Funktion (Sisbkup. h)
description: Gibt durch SIS-API-Funktionen zugeordnete Speicher frei.
ms.assetid: 8fab79c8-593c-46df-a885-09a59620a977
keywords:
- Sisfrezugeredmemory-Funktions Sicherung
topic_type:
- apiref
api_name:
- SisFreeAllocatedMemory
api_location:
- Sisbkup.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 724970817b89f6a9f2490b0776775f6a3a4e69ca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858760"
---
# <a name="sisfreeallocatedmemory-function"></a>Sisfrezugeredmemory-Funktion

Die Funktion " **sisfrezugenspeicher** " gibt durch SIS-API-Funktionen zugewiesene Arbeitsspeicher frei.

## <a name="syntax"></a>Syntax


```C++
void SisFreeAllocatedMemory(
  _In_ PVOID allocatedSpace
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*zustellspeicherplatz* \[ in\]
</dt> <dd>

Zeiger auf den Arbeitsspeicher, der von der SIS-API zugeordnet wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Nachdem der Aufruf dieser Funktion abgeschlossen ist, kann der Aufrufer nicht mehr auf den freigegebenen Speicher zugreifen.

Dieser Befehl sollte verwendet werden, um den zugeordneten Arbeitsspeicher für die Parameter Zeichenfolgen von *commonstorerootpathname* , die von " [**siscreatebackupstructure**](siscreatebackupstructure.md) " und " [**siscreaterestorestruktur**](siscreaterestorestructure.md)" zurückgegeben werden, und das Array von Zeichen folgen, das die Namen der allgemeinen Speicherdateien enthält, die von **siscreatebackupstructure**, [**siscsfilestobackupforlink**](siscsfilestobackupforlink.md), **siscreaterestorestruktur** und [**sisrestoredlink**](sisrestoredlink.md)zurückgegeben werden. Im letzteren Fall muss das Array selbst freigegeben werden, indem **sisfrezugedmemory** aufgerufen wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                   |
| Header<br/>                   | <dl> <dt>Sisbkup. h</dt> </dl>   |
| Bibliothek<br/>                  | <dl> <dt>Sisbkup. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Sisbkup.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Siscreatebackupstructure**](siscreatebackupstructure.md)
</dt> <dt>

[**Siscreaterestorestruktur**](siscreaterestorestructure.md)
</dt> <dt>

[**Siscsfilestobackupforlink**](siscsfilestobackupforlink.md)
</dt> <dt>

[**Sisrestoredlink**](sisrestoredlink.md)
</dt> </dl>

 

 





