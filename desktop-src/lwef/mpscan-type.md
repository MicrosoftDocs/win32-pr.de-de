---
title: MPSCAN_TYPE-Enumeration (MpClient.h)
description: Typ der durchgeführten Überprüfung.
ms.assetid: 980A80FD-FF02-4338-B7FB-DAA141F65E89
keywords:
- MPSCAN_TYPE enumeration Legacy Windows Environment Features
- PMPSCAN_TYPE enumeration pointer Legacy Windows Environment Features
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
ms.openlocfilehash: 56906bfc9ad57f93bac4c8b8c27360b5ade9592ac33efe39574fe8890299e13a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118747131"
---
# <a name="mpscan_type-enumeration"></a>MPSCAN \_ TYPE-Enumeration

Typ der durchgeführten Überprüfung.

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

<span id="MPSCAN_TYPE_UNKNOWN"></span><span id="mpscan_type_unknown"></span>**\_MPSCAN-TYP \_ UNBEKANNT**
</dt> <dd>

Nur interne Verwendung.

</dd> <dt>

<span id="MPSCAN_TYPE_QUICK"></span><span id="mpscan_type_quick"></span>**\_MPSCAN-TYP \_ : SCHNELL**
</dt> <dd>

Scannt ausgeführte Prozesse und verschiedene ASEP-Punkte im System, wo Schadsoftware in der Regel ausblendet.

</dd> <dt>

<span id="MPSCAN_TYPE_FULL"></span><span id="mpscan_type_full"></span>**\_MPSCAN-TYP \_ FULL**
</dt> <dd>

Führt eine Schnellprüfung durch, gefolgt von einer Überprüfung aller Festplattenlaufwerke des Systems.

</dd> <dt>

<span id="MPSCAN_TYPE_RESOURCE"></span><span id="mpscan_type_resource"></span>**\_ \_ MPSCAN-TYPRESSOURCE**
</dt> <dd>

Scannt bestimmte Ressourcen, z. B. Dateien oder Ordner.

</dd> <dt>

<span id="MPSCAN_TYPE_MAXVALUE"></span><span id="mpscan_type_maxvalue"></span>**\_MPSCAN-TYP \_ MAXVALUE**
</dt> <dd>

Maximalwert möglich.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>MpClient.h</dt> </dl> |



 

 





