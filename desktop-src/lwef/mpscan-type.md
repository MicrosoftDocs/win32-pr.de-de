---
title: MPSCAN_TYPE-Enumeration (mpclient. h)
description: Der Typ des ausgeführten Scans.
ms.assetid: 980A80FD-FF02-4338-B7FB-DAA141F65E89
keywords:
- MPSCAN_TYPE-Enumerationsfunktionen der Legacy-Windows-Umgebung
- PMPSCAN_TYPE enumerationszeiger Legacy-Windows-Umgebungs Features
topic_type:
- apiref
api_name:
- MPSCAN_TYPE
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9eb89137dc9cfe5b8a4ff1f44a7a101239aa3a22
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740136"
---
# <a name="mpscan_type-enumeration"></a>Mpscan- \_ Typenumeration

Der Typ des ausgeführten Scans.

## <a name="syntax"></a>Syntax


```C++
typedef enum tagMPSCAN_TYPE { 
  MPSCAN_TYPE_UNKNOWN   = 0,
  MPSCAN_TYPE_QUICK     = 1,
  MPSCAN_TYPE_FULL      = 2,
  MPSCAN_TYPE_RESOURCE  = 3,
  MPSCAN_TYPE_MAXVALUE  = 3
} MPSCAN_TYPE, *PMPSCAN_TYPE;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="MPSCAN_TYPE_UNKNOWN"></span><span id="mpscan_type_unknown"></span>**mpscan- \_ Typ \_ unbekannt**
</dt> <dd>

Nur interne Verwendung.

</dd> <dt>

<span id="MPSCAN_TYPE_QUICK"></span><span id="mpscan_type_quick"></span>**mpscan- \_ Typ \_ Quick**
</dt> <dd>

Scannt laufende Prozesse und verschiedene ASEP-Punkte im System, wo Schadsoftware normalerweise ausgeblendet wird.

</dd> <dt>

<span id="MPSCAN_TYPE_FULL"></span><span id="mpscan_type_full"></span>**mpscan- \_ Typ \_ voll**
</dt> <dd>

Führt eine schnell Überprüfung durch, gefolgt von der Überprüfung aller Festplattenlaufwerke des Systems.

</dd> <dt>

<span id="MPSCAN_TYPE_RESOURCE"></span><span id="mpscan_type_resource"></span>**mpscan \_ - \_ typressource**
</dt> <dd>

Scannt bestimmte Ressourcen, z. b. Dateien oder Ordner.

</dd> <dt>

<span id="MPSCAN_TYPE_MAXVALUE"></span><span id="mpscan_type_maxvalue"></span>**mpscan- \_ Typ \_ MaxValue**
</dt> <dd>

Maximal möglicher Wert.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Mpclient. h</dt> </dl> |



 

 





