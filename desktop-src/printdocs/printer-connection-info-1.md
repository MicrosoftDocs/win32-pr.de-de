---
description: Stellt Informationen zu einer Verbindung mit einem Drucker dar.
ms.assetid: afac3f91-74eb-46f7-94b4-d37b2b8a32a4
title: PRINTER_CONNECTION_INFO_1 -Struktur (Winspool.h)
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
ms.openlocfilehash: b9adbe18d3f75062a67440fd7f7586c4336323ff3035416f3ad9799f5e34a17e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119033898"
---
# <a name="printer_connection_info_1-structure"></a>STRUKTUR \_ DER \_ \_ DRUCKERVERBINDUNGSINFORMATIONEN 1

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
| \_ \_ DRUCKERVERBINDUNGSKONFLIKT (0X00000020) | Wenn dieses Bitflag festgelegt ist, ist die Druckerverbindung nicht übereinstimmend. Der Benutzer kann einen lokalen Druckertreiber als *pszDriverName* angeben und für das Rendering verwenden, anstatt den Treiber zu verwenden, der auf dem Serverdrucker installiert ist, mit dem der Benutzer verbunden ist.<br/>                                                                                                                                                                                                                                    |
| DRUCKERVERBINDUNG \_ \_ OHNE \_ BENUTZEROBERFLÄCHE (0x00000040)   | Wenn dieses Bitflag festgelegt ist, kann bei diesem Aufruf kein Dialogfeld angezeigt werden. Wenn ein Dialogfeld angezeigt werden muss, um einen Druckertreiber vom Server zu installieren, und dieses Bitflag festgelegt ist, wird der Druckertreiber nicht installiert, die Druckerverbindung wird nicht hinzugefügt, und der Aufruf ist nicht möglich.<br/> **Windows 7:** Wenn Windows 7 und höhere Versionen von Windows festgelegt ist und der Benutzer im Modus mit erhöhten Rechten ausgeführt wird, wird das Dialogfeld Vertrauenswürdiger **Drucker?** nicht angezeigt.<br/> |



 

</dd> <dt>

**pszDriverName**
</dt> <dd>

Ein Zeiger auf den Namen des Treibers.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                                            |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Drucken von Spooler-API-Strukturen](printing-and-print-spooler-structures.md)
</dt> </dl>

 

 




