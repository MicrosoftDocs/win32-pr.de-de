---
description: 'Weitere Informationen finden Sie unter: JET_SNT'
title: JET_SNT
TOCTitle: JET_SNT
ms:assetid: 74ac5142-8102-4dd3-8f2a-786a7a2ac78f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269294(v=EXCHG.10)
ms:contentKeyID: 32765586
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
ms.openlocfilehash: 250ad992ec26b218bab21691f26c0938b6be6921
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122481386"
---
# <a name="jet_snt"></a>JET_SNT


_**Gilt für:** Windows | Windows Server_

## <a name="jet_snt"></a>JET_SNT

Die [JET_SNT]() Gruppe von Konstanten beschreibt die Punkte des Fortschritts eines Vorgangs, zu dem Informationen in einem Aufruf der rückruffunktion JET_PFNSTATUS [werden.](./jet-pfnstatus-callback-function.md)


| <p>Konstante/Wert</p> | <p>BESCHREIBUNG</p> | 
|-----------------------|--------------------|
| <p>JET_sntBegin<br />5</p> | <p>Der Anfang eines Vorgangs</p> | 
| <p>JET_sntRequirements<br />7</p> | <p>Wird nicht unterstützt.</p><p><strong>Windows 2000 Server:</strong>  Der Vorgang wird gestartet. In diesem Fall sollte der letzte Parameter der Rückruffunktion ein <a href="gg269328(v=exchg.10).md"></a> gültiger Zeiger auf eine JET_SNPROG-Struktur sein, die die Gesamtzahl der auszuführenden Einheiten angibt.</p> | 
| <p>JET_sntProgress<br />0</p> | <p>Die Anzahl der abgeschlossenen Einheiten und die Anzahl der noch zu erledigenden Einheiten. Diese Informationen werden in den Membern einer <a href="gg269328(v=exchg.10).md">JET_SNPROG</a> zurückgegeben.</p> | 
| <p>JET_sntComplete<br />6</p> | <p>Der Abschluss eines Vorgangs.</p> | 
| <p>JET_sntFail<br />3</p> | <p>Der Fehler eines Vorgangs.</p> | 
| <p>JET_sntRecoveryStep<br />8</p> | <p>Die Wiederherstellungssteuerung eines Vorgangs.</p><div class="alert">&gt; [!NOTE]&gt; <P>Dieser Wert gilt nicht für Versionen des Windows Betriebssystems, beginnend mit Windows 8.</P></div> | 



### <a name="requirements"></a>Anforderungen


| | | <p><strong>Client</strong></p> | <p>Erfordert Windows Vista, Windows XP oder Windows 2000 Professional.</p> | | <p><strong>Server</strong></p> | <p>Erfordert Windows Server 2008, Windows Server 2003 oder Windows 2000 Server.</p> | | <p><strong>Header</strong></p> | <p>Wird in Esent.h deklariert.</p> | 



### <a name="see-also"></a>Weitere Informationen

[JET_PFNSTATUS](./jet-pfnstatus-callback-function.md)  
[JET_SNP](./jet-snp.md)  
[JET_SNPROG](./jet-snprog-structure.md)
