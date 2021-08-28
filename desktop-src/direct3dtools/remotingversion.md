---
description: Eine Enumeration, mit der angegeben wird, welche Version des Remoting-Protoculs verwendet wird.
MS-HAID: vspixengine.REMOTINGVERSION
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: REMOTINGVERSION-Enumeration
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 598E9586-05FF-4889-BBAF-44814EEF203A
api_name:
- REMOTINGVERSION
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 121342a2c0d47b2041893459d577e09e3b4d73ba
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2021
ms.locfileid: "122627235"
---
# <a name="span-idvspixengineremotingversionspanremotingversion-enumeration"></a><span id="vspixengine.remotingversion"></span>REMOTINGVERSION-Enumeration

Eine Enumeration, mit der angegeben wird, welche Version des Remoting-Protoculs verwendet wird.

## <a name="syntax"></a>Syntax


```C++
};
```

## <a name="constants"></a>Konstanten

<span id="REMOTING_DEV12"></span><span id="remoting_dev12"></span>**REMOTING \_ DEV12**  
Ein -Wert, der angibt, dass das Visual Studio 2013 RTM-Remotingprotokoll verwendet wird.

<span id="REMOTING_DEV12_UPDATE_1"></span><span id="remoting_dev12_update_1"></span>**REMOTING \_ DEV12 \_ UPDATE \_ 1**  
Ein -Wert, der angibt, dass das Visual Studio 2013 Update 1-Remotingprotokoll verwendet wird.

<span id="REMOTING_DEV12_UPDATE_4"></span><span id="remoting_dev12_update_4"></span>**REMOTING \_ DEV12 \_ UPDATE \_ 4**  
Ein -Wert, der angibt, dass das Visual Studio 2013 Update 4 Remotingprotokoll verwendet wird.

<span id="REMOTING_DEV14"></span><span id="remoting_dev14"></span>**REMOTING \_ DEV14**  
Ein -Wert, der angibt, dass das Visual Studio 2015 RTM-Remotingprotokoll verwendet wird.

<span id="REMOTING_WIN10"></span><span id="remoting_win10"></span>**REMOTING \_ WIN10**  
Ein -Wert, der angibt, dass das Windows 10 Remotingprotokoll verwendet wird (ab Windows 10 ist die Grafikdiagnose eine Betriebssystemkomponente).

<span id="REMOTING_WIN10_JAN_2015"></span><span id="remoting_win10_jan_2015"></span>**REMOTING \_ WIN10 \_ JAN \_ 2015**  
Ein -Wert, der angibt, dass das remoting-Protokoll Windows 10 (Januar 2015) verwendet wird.

<span id="REMOTING_WIN10_JAN_2015_1"></span><span id="remoting_win10_jan_2015_1"></span>**REMOTING \_ WIN10 \_ JAN \_ 2015 \_ 1**  
Ein -Wert, der angibt, dass das remoting-Protokoll Windows 10 (Januar 2015, v1) verwendet wird.

<span id="REMOTING_WIN10_JAN_2015_2"></span><span id="remoting_win10_jan_2015_2"></span>**REMOTING \_ WIN10 \_ JAN \_ 2015 \_ 2**  
Ein -Wert, der angibt, dass das Windows 10 Remotingprotokoll (Januar 2015, v2) verwendet wird. Mit dieser Version des Protokolls wurden Anforderungen zum Visualisieren von gekachelten Ressourcen eingeführt.

<span id="REMOTING_WIN10_JAN_2015_3"></span><span id="remoting_win10_jan_2015_3"></span>**REMOTING \_ WIN10 \_ JAN \_ 2015 \_ 3**  
Ein -Wert, der angibt, dass das remoting-Protokoll Windows 10 (Januar 2015, v3) verwendet wird. Mit dieser Version des Protokolls wurde IPixEngine7 eingeführt, das jetzt veraltet ist, um die Unterstützung der Schnittstellenversion zu überprüfen.

<span id="REMOTING_IPIXENGINE7_VERSION_CHECKING"></span><span id="remoting_ipixengine7_version_checking"></span>**ÜBERPRÜFEN DER VERSION VON REMOTING \_ IPIXENGINE7 \_ \_**  
Ein -Wert, der angibt, dass das remoting-Protokoll Windows 10 (Januar 2015, v1) verwendet wird. Diese Version des Protokolls verlässt sich nicht mehr auf REMOTINGVERSION, um Protokollfunktionen zu vermitteln. Die Schnittstellen-GUID wird jetzt geändert, wenn nicht öffentlich int

<span id="REMOTING_WIN10_FEB_2015_1"></span><span id="remoting_win10_feb_2015_1"></span>**REMOTING \_ WIN10 \_ FEB \_ 2015 \_ 1**  
Ein -Wert, der angibt, dass das remoting-Protokoll Windows 10 (Januar 2015, v1) verwendet wird. Diese Version des Protokolls führt Zusammenfassungsinformationseigenschaften mit eindeutigen, festen IDs ein.

<span id="REMOTING_WIN10_2015_03_00"></span><span id="remoting_win10_2015_03_00"></span>**REMOTING \_ WIN10 \_ 2015 \_ 03 \_ 00**  
Ein -Wert, der angibt, dass das remoting-Protokoll Windows 10 (Januar 2015, v1) verwendet wird. Mit dieser Version des Protokolls wurde unterstützung für das DirectX11-Statusfenster eingeführt.

<span id="REMOTING_LATES"></span><span id="remoting_lates"></span>**REMOTING \_ LATES**  
Ein -Wert, der angibt, dass das neueste Remotingprotokoll verwendet wird.

## <a name="requirements"></a>Requirements (Anforderungen)

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Header</p></td><td>Vspixengine.h</td></tr></tbody></table>

 

 



