---
description: 'Weitere Informationen finden Sie unter: JET_SNP'
title: JET_SNP
TOCTitle: JET_SNP
ms:assetid: 7f3d1cc5-7b27-454d-8dd1-584ab4b60ab0
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269311(v=EXCHG.10)
ms:contentKeyID: 32765601
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
ms.openlocfilehash: ee83dc86aa6faf5fab0b45596a586c657e4c6e2a
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122474126"
---
# <a name="jet_snp"></a>JET_SNP


_**Gilt für:** Windows | Windows Server_

## <a name="jet_snp"></a>JET_SNP

Die **JET_SNP** Gruppe von Konstanten beschreibt den Typ des Vorgangs, für den Statusinformationen erhalten werden sollen. Diese Konstanten werden als *snp-Parameter* der [JET_PFNSTATUS-Rückruffunktion](./jet-pfnstatus-callback-function.md) verwendet.


| <p>Konstante/Wert</p> | <p>BESCHREIBUNG</p> | 
|-----------------------|--------------------|
| <p>JET_snpRepair<br />2</p> | <p>Der Rückruf ist für einen Reparaturvorgang.</p> | 
| <p>JET_snpCompact<br />4</p> | <p>Der Rückruf ist für die Datenbankdefragmentierung.</p> | 
| <p>JET_snpRestore<br />8</p> | <p>Der Rückruf ist für einen Wiederherstellungsvorgang.</p> | 
| <p>JET_snpBackup<br />9</p> | <p>Der Rückruf ist für einen Sicherungsvorgang.</p> | 
| <p>JET_snpUpgrade<br />10</p> | <p>Wird nicht unterstützt.</p><p><strong>Windows 2000:</strong>  Der Rückruf ist für den Upgradevorgang im Datenbankformat.</p> | 
| <p>JET_snpScrub<br />11</p> | <p>Der Rückruf ist für einen Datenbank-Zeroing-Vorgang (d. h. bereinigung) zu verwenden.</p><p><strong>Windows Server 2003 und Windows 2000 Server:</strong>  Nicht unterstützt.</p> | 
| <p>JET_snpUpgradeRecordFormat<br />12</p> | <p>Der Rückruf ist für das Upgrade des Datensatzformats aller Datenbankseiten.</p><p><strong>Windows Server 2003 und Windows 2000 Server:</strong>  Nicht unterstützt.</p> | 



### <a name="requirements"></a>Anforderungen


| | | <p><strong>Client</strong></p> | <p>Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</p> | | <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</p> | | <p><strong>Header</strong></p> | <p>Wird in Esent.h deklariert.</p> | 



### <a name="see-also"></a>Weitere Informationen

[JET_PFNSTATUS](./jet-pfnstatus-callback-function.md)  
[JET_SNPROG](./jet-snprog-structure.md)  
[JET_SNT](./jet-snt.md)
