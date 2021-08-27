---
description: 'Weitere Informationen finden Sie unter: JET_LS'
title: JET_LS
TOCTitle: JET_LS
ms:assetid: 8e4e7902-84b1-404b-8654-bb430a0952aa
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269336(v=EXCHG.10)
ms:contentKeyID: 32765625
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
ms.openlocfilehash: 82a0df37215122e943955f32aeed4d39dd70b268
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122983153"
---
# <a name="jet_ls"></a>JET_LS


_**Gilt für:** Windows | Windows Server_

## <a name="jet_ls"></a>JET_LS

Der **JET_LS-Datentyp** enthält ein Kontexthandl für den lokalen Speicher (LS). Dieses Handle kann einem Cursor oder einer Tabelle zugeordnet sein und auf dynamisch zugeordnete Ressourcen verweisen.

**Windows XP: JET_LS** wird in xp Windows eingeführt.

```cpp
    typedef JET_API_PTR JET_LS;
```

### <a name="data-types"></a>Datentypen

JET_LS

Der Wert JET_LSNil gibt ein ungültiges Kontexthand handle an.

### <a name="remarks"></a>Bemerkungen

Ein Kontexthandl wird anfänglich mithilfe von [JetSetLS](./jetsetls-function.md) **dem** JET_LS zugeordnet. Das Kontexthandl kann mithilfe von **JetGetLS aus** dem JET_LS [abgerufen werden.](./jetgetls-function.md)

Die Zuordnung des Kontexthandls zum Datentyp  JET_LS mit [JetGetLS](./jetgetls-function.md) kann explizit JET_bitLSReset. Alternativ kann das Kontexthand handle implizit vom **JET_LS-Datentyp** disassoziiert werden, wenn das zugrunde liegende Objekt von der Datenbank-Engine als Folge einer direkten oder indirekten Aktion durch die Anwendung freigegeben wird. Im impliziten Fall wird ein Laufzeitrückruf an die Anwendung ausgegeben, damit sie das Kontexthand handle bereinigen kann. Weitere Informationen zur impliziten Disassoziierung vom **JET_LS-Datentyp** finden Sie unter [JetSetLS](./jetsetls-function.md).

Die folgenden Flags sind dem JET_LS zugeordnet.


| <p>Begriff</p> | <p>BESCHREIBUNG</p> | 
|-------------|--------------------|
| <p>JET_bitLSReset</p> | <p>Die Zuordnung des Kontexthandpunkts zum -Objekt wird entfernt.</p> | 
| <p>JET_bitLSCursor</p> | <p>Legen Sie den lokalen Speicher fest, der einem Tabellencursor zugeordnet ist, oder rufen Sie diesen ab.</p> | 
| <p>JET_bitLSTable</p> | <p>Legen Sie den lokalen Speicher fest, der einer Tabelle zugeordnet ist, oder rufen Sie diesen ab.</p> | 
| <p>JET_LSNil</p> | <p>Das Kontexthand handle ist ungültig.</p> | 



### <a name="requirements"></a>Anforderungen


| Anforderung | Wert |
|------------|----------|
| <p><strong>Client</strong></p> | <p>Erfordert Windows Vista oder Windows XP.</p> | 
| <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008 oder Windows Server 2003.</p> | 
| <p><strong>Header</strong></p> | <p>Wird in Esent.h deklariert.</p> | 



### <a name="see-also"></a>Weitere Informationen

[JetSetLS](./jetsetls-function.md)  
[JetGetLS](./jetgetls-function.md)
