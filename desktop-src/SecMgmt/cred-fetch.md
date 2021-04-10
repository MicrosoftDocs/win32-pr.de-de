---
description: Definiert Werte, die bestimmen, wie die Anmelde Informationen eines Gruppen verwalteten Dienst Kontos (GMSA) abgerufen werden.
ms.assetid: 90891448-22F6-497A-A612-3DAB8622C325
title: CRED_FETCH-Enumeration (secpkg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRED_FETCH
api_type:
- HeaderDef
api_location:
- Secpkg.h
ms.openlocfilehash: 6a7c30f29826b017bc7a3badd796955ec31a1ca7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960258"
---
# <a name="cred_fetch-enumeration"></a>Fed- \_ Fetch-Enumeration

Definiert Werte, die bestimmen, wie die Anmelde Informationen eines Gruppen verwalteten Dienst Kontos (GMSA) abgerufen werden.

## <a name="syntax"></a>Syntax


```C++
typedef enum _CRED_FETCH { 
  CredFetchDefault  = 0,
  CredFetchDPAPI    = 1,
  CredFetchForced   = 2
} CRED_FETCH;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="CredFetchDefault"></span><span id="credfetchdefault"></span><span id="CREDFETCHDEFAULT"></span>**"Kredfetchdefault"**
</dt> <dd>

Gibt an, dass das Betriebssystem zuerst versuchen soll, das Kennwort aus dem lokalen Cache abzurufen. Wenn es an der Zeit ist, das Kennwort abzurufen, sollte das Betriebssystem eine Verbindung mit einem Domänen Controller für das Kennwort aufnehmen. Wenn dies nicht möglich ist, geben Sie alle zwischengespeicherten Kenn Wörter mit dem Statuswert Erfolg zurück.

</dd> <dt>

<span id="CredFetchDPAPI"></span><span id="credfetchdpapi"></span><span id="CREDFETCHDPAPI"></span>**"Kredfetchdpapi"**
</dt> <dd>

Gibt die lokalen DPAPI-Anmelde Informationen an den Aufrufer zurück. SSPs ( [*Security Support Providers*](/windows/desktop/SecGloss/s-gly) ) erfordern im Allgemeinen nicht die Verwendung dieser Enumeration.

</dd> <dt>

<span id="CredFetchForced"></span><span id="credfetchforced"></span><span id="CREDFETCHFORCED"></span>**"Kredfetchforced"**
</dt> <dd>

Erzwingt, dass das Betriebssystem versucht, das Kennwort vom Domänen Controller zu lesen. Während der Kenn Wort rolloverzeit wurde das Kennwort möglicherweise auf dem Domänen Controller und anderen Mitglieds Hosts geändert, aber der GMSA-Mitglieds Host erkennt das Kennwort als noch gültig. Dies kann auf Probleme mit der Takt Abweichung zwischen verschiedenen Domänen Controllern zurückzuführen sein. Wenn dieser Wert angegeben ist, bestimmt das Betriebssystem, ob eine mögliche Kenn Wort Änderung aufgrund einer Zeit Abweichung möglich wäre, und ruft das Kennwort ab, wenn dies der Fall ist. Andernfalls werden die zwischengespeicherten Anmelde Informationen zurückgegeben. Wenn keine zwischengespeicherten Anmelde Informationen vorhanden sind, versucht das Betriebssystem, eine vom Domänen Controller zu erhalten.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Secpkg. h</dt> </dl> |



 

