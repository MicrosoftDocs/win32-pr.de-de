---
title: SisFreeAllocatedMemory-Funktion (Sisbkup.h)
description: Gibt von SIS-API-Funktionen zugeordneten Arbeitsspeicher frei.
ms.assetid: 8fab79c8-593c-46df-a885-09a59620a977
keywords:
- SisFreeAllocatedMemory-Funktionssicherung
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
ms.openlocfilehash: a4510e464c2201952823d144721614caa7b5f1397c68f4f129dac73a4015b86a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119702180"
---
# <a name="sisfreeallocatedmemory-function"></a>SisFreeAllocatedMemory-Funktion

Die **SisFreeAllocatedMemory-Funktion gibt** von SIS-API-Funktionen zugeordneten Arbeitsspeicher frei.

## <a name="syntax"></a>Syntax


```C++
void SisFreeAllocatedMemory(
  _In_ PVOID allocatedSpace
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*allocatedSpace* \[ In\]
</dt> <dd>

Zeiger auf den von der SIS-API zugeordneten Arbeitsspeicher.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Nach Abschluss des Aufrufs dieser Funktion kann der Aufrufer möglicherweise nicht mehr auf den freien Arbeitsspeicher zugreifen.

Dieser Aufruf sollte verwendet werden, um die Speicherbelegung für die *commonStoreRootPathname-Parameterzeichenfolgen,* die von [**SisCreateBackupStructure**](siscreatebackupstructure.md) und [**SisCreateRestoreStructure**](siscreaterestorestructure.md)zurückgegeben werden, und das Array von Zeichenfolgen mit allgemeinen Speicherdateinamen, die von **SisCreateBackupStructure,** [**SisCSFilesToBackupForLink,**](siscsfilestobackupforlink.md) **SisCreateRestoreStructure** und [**SisRestoredLink**](sisrestoredlink.md)zurückgegeben werden, aufzuberäumen. Im letzteren Fall muss auch das Array selbst durch Aufrufen von **SisFreeAllocatedMemory frei werden.**

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ XP-Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                   |
| Header<br/>                   | <dl> <dt>Sisbkup.h</dt> </dl>   |
| Bibliothek<br/>                  | <dl> <dt>Sisbkup.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Sisbkup.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**SisCreateBackupStructure**](siscreatebackupstructure.md)
</dt> <dt>

[**SisCreateRestoreStructure**](siscreaterestorestructure.md)
</dt> <dt>

[**SisCSFilesToBackupForLink**](siscsfilestobackupforlink.md)
</dt> <dt>

[**SisRestoredLink**](sisrestoredlink.md)
</dt> </dl>

 

 





