---
description: Stellt Informationen zu einer Verbindung mit einem Drucker dar.
ms.assetid: afac3f91-74eb-46f7-94b4-d37b2b8a32a4
title: PRINTER_CONNECTION_INFO_1 Struktur (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_CONNECTION_INFO_1
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 04bfb5411a5602248bcd188d07dec8478462fd2f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757381"
---
# <a name="printer_connection_info_1-structure"></a>Drucker \_ Verbindungs \_ Info \_ 1-Struktur

Stellt Informationen zu einer Verbindung mit einem Drucker dar.

## <a name="syntax"></a>Syntax


```C++
typedef struct _PRINTER_CONNECTION_INFO_1 {
  DWORD  dwFlags;
  LPTSTR pszDriverName;
} PRINTER_CONNECTION_INFO_1, *PPRINTER_CONNECTION_INFO_1;
```



## <a name="members"></a>Member

<dl> <dt>

**dwFlags**
</dt> <dd>

Die folgenden Werte sind definiert:



| Wert                                      | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|--------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Fehler bei der Drucker \_ Verbindung \_ (0x00000020). | Wenn dieses Bitflag festgelegt ist, stimmt die Druckerverbindung nicht überein. Der Benutzer kann einen lokalen Druckertreiber als *pszdrivername* angeben und ihn verwenden, um das Rendering durchzuführen, anstatt den Treiber zu verwenden, der auf dem Server Drucker installiert ist, mit dem der Benutzer verbunden ist.<br/>                                                                                                                                                                                                                                    |
| Drucker \_ Verbindung \_ keine \_ Benutzeroberfläche (0x00000040)   | Wenn dieses Bitflag festgelegt ist, kann dieser Befehl kein Dialogfeld anzeigen. Wenn ein Dialogfeld angezeigt werden muss, um einen Druckertreiber vom Server zu installieren, und dieses Bitflag festgelegt ist, wird der Druckertreiber nicht installiert, die Druckerverbindung wird nicht hinzugefügt, und der-Rückruf schlägt fehl.<br/> **Windows 7:** Wenn dieses Flag in Windows 7 und höheren Versionen von Windows festgelegt ist und der Benutzer im Modus mit erhöhten Rechten ausgeführt wird, wird das Dialogfeld vertrauenswürdig für **diesen Drucker?** nicht angezeigt.<br/> |



 

</dd> <dt>

**pszdrivername**
</dt> <dd>

Ein Zeiger auf den Namen des Treibers.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                                            |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool. h (Include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Druck Spooler-API-Strukturen](printing-and-print-spooler-structures.md)
</dt> </dl>

 

 




