---
description: 'Weitere Informationen zu: Ungültige Handlekonstanten'
title: Ungültige Handlekonstanten
TOCTitle: Invalid Handle Constants
ms:assetid: 594d7804-725f-4f72-b5f0-56f099c1c17b
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269256(v=EXCHG.10)
ms:contentKeyID: 32765558
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 28a52b2fc7a51572cc7bb78ad7631df41438310a
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122473276"
---
# <a name="invalid-handle-constants"></a>Ungültige Handlekonstanten


_**Gilt für:** Windows | Windows Server_

## <a name="invalid-handle-constants"></a>Ungültige Handlekonstanten

Die folgenden Konstanten weisen auf ungültige Handles für verschiedene Ese-Aspekte hin.


| <p>Konstante/Wert</p> | <p>BESCHREIBUNG</p> | 
|-----------------------|--------------------|
| <p>JET_instanceNil<br />(~(JET_INSTANCE)0)</p> | <p>Ein ungültiges Handle für eine Datenbankinstanz.<br /><strong>Windows XP:</strong> Eingeführt in Windows XP.</p> | 
| <p>JET_sesidNil<br />(~(JET_SESID)0)</p> | <p>Ein ungültiges Handle für eine Sitzungs-ID.</p> | 
| <p>JET_tableidNil<br />(~(JET_TABLEID)0)</p> | <p>Ein ungültiges Handle für eine Tabellen-ID.</p> | 
| <p>JET_bitNil<br />((JET_GRBIT)0)</p> | <p>Ein ungültiges Handle für eine Gruppe von Bits.</p> | 
| <p>JET_LSNil<br />(~(JET_LS)0)</p> | <p>Ein ungültiges Handle für die lokale Storage.</p> | 
| <p>JET_dbidNil<br />((JET_DBID) 0xFFFFFFFF)</p> | <p>Ein ungültiges Handle für die Datenbank-ID.</p> | 



### <a name="requirements"></a>Anforderungen


| | | <p><strong>Client</strong></p> | <p>Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</p> | | <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</p> | | <p><strong>Header</strong></p> | <p>Deklariert in Esent.h.</p> | 


