---
description: Die isvaliddevmode-Funktion überprüft, ob der Inhalt einer DEVMODE-Struktur gültig ist.
ms.assetid: 8b4e32cc-5eeb-4a0d-a1b7-f6edb99ed8d8
title: Isvaliddevmode-Funktion (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IsValidDevmode
- IsValidDevmodeA
- IsValidDevmodeW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 0b8a940fd08e1ab19b18969a763448b65fffd9d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352732"
---
# <a name="isvaliddevmode-function"></a>Isvaliddevmode-Funktion

Die **isvaliddevmode** -Funktion überprüft, ob der Inhalt einer DEVMODE-Struktur gültig ist.

## <a name="syntax"></a>Syntax


```C++
BOOL IsValidDevmode(
  _In_ PDEVMODE pDevmode,
       size_t   DevmodeSize
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pdevmode* \[ in\]
</dt> <dd>

Ein Zeiger auf den zu validierenden [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) .

</dd> <dt>

*Devmudesize* 
</dt> <dd>

Die Größe des Eingabe Byte Puffers in Bytes.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

**True**, wenn der [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) -Wert strukturell gültig ist. Wenn kleinere Fehler gefunden werden, werden Sie von der Funktion behoben und **true** zurückgegeben.

**False**, wenn der [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) ein oder mehrere bedeutende strukturellen Probleme aufweist. Beispielsweise ist der **dmsize** -Member falsch ausgerichtet oder gibt einen zu kleinen Puffer an. Außerdem **false** , wenn **pdevmode** **null** ist.

## <a name="remarks"></a>Bemerkungen

Es werden keine privaten Druckertreiber Felder des [**DEVMODE-Modus**](/windows/win32/api/wingdi/ns-wingdi-devmodea) geprüft, sondern nur die öffentlichen Felder.

Aufrufer sollten **dmsize** + **dmdriverextra** für **devmudesize** nur verwenden, wenn Sie sicherstellen können, dass die Eingabepuffergröße mindestens so groß ist. Da es sich bei [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) im Allgemeinen um nicht vertrauenswürdige Daten handelt, sind die Werte, die im Eingabepuffer in den Offsets **dmsize** und **dmdriverextra** liegen, ebenfalls nicht vertrauenswürdig.

Diese Funktion ist im Lua-Kontext (Least-Privileged User Account) ausführbare Datei.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Winspool. h</dt> </dl>   |
| Bibliothek<br/>                  | <dl> <dt>Winspool. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Winspool. drv</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **Isvaliddevmodew** (Unicode) und **isvaliddevmodea** (ANSI)<br/>                 |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Druckspooler-API-Funktionen](printing-and-print-spooler-functions.md)
</dt> <dt>

[**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea)
</dt> </dl>

 

 




