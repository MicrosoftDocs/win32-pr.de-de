---
description: Konvertiert klein geschriebene Zeichen in einem Puffer in Großbuchstaben.
ms.assetid: 63293fda-6f55-419a-b5b4-7a3ada31580c
title: Charupperbuffwrapw-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CharUpperBuffWrapW
api_type:
- DllExport
api_location:
- Shlwapi.dll
ms.openlocfilehash: dacc5e7609ca7f91bf7c66651d7ba9bdd11ab688
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525397"
---
# <a name="charupperbuffwrapw-function"></a>Charupperbuffwrapw-Funktion

\[**Charupperbuffwrapw** ist für die Verwendung in Windows XP verfügbar. Sie ist möglicherweise in nachfolgenden Versionen nicht verfügbar. Sie sollten an seiner Stelle [**charupperbuffw**](/windows/win32/api/winuser/nf-winuser-charupperbuffa) verwenden.\]

Konvertiert klein geschriebene Zeichen in einem Puffer in Großbuchstaben. Die-Funktion konvertiert die Zeichen an Ort und Stelle.

> [!Note]  
> **Charupperbuffwrapw** ist ein Wrapper für die **charupperbuffw** -Funktion. Weitere Hinweise zur Verwendung finden Sie auf der Seite [**charupperbuff**](/windows/win32/api/winuser/nf-winuser-charupperbuffa) .

 

## <a name="syntax"></a>Syntax


```C++
DWORD CharUpperBuffWrapW(
  _In_ LPWSTR pch,
  _In_ DWORD  cchLength
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*PCH* \[ in\]
</dt> <dd>

Typ: **LPWSTR**

Ein Zeiger auf einen Puffer, der ein oder mehrere zu verarbeitende Unicode-Zeichen enthält.

</dd> <dt>

*cchlength* \[ in\]
</dt> <dd>

Typ: **DWORD**

Gibt die Größe des Puffers, auf den *PCH* zeigt, in Zeichen an.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **DWORD**

Die Anzahl der verarbeiteten Zeichen.

## <a name="remarks"></a>Bemerkungen

Die bevorzugte Methode ist die Verwendung von [**charupperbuffw**](/windows/win32/api/winuser/nf-winuser-charupperbuffa) in Verbindung mit der Microsoft-Schicht für Unicode (MSLU).

**Charupperbuffwrapw** muss direkt aus Shlwapi.dll aufgerufen werden, und zwar mithilfe der Ordinalzahl 44.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional, Windows XP \[ Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shlwapi.dll (Version 5,0 oder höher)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Charupperbuff**](/windows/win32/api/winuser/nf-winuser-charupperbuffa)
</dt> </dl>

 

 
