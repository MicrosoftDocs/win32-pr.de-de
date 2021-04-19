---
description: Ruft eine Bitmaske ab, die die im System verfügbaren Produkt Suites identifiziert. Wenn diese Funktion in einer Anwendung aufgerufen wird, die im Kontext eines Server Silos ausgeführt wird, wird stattdessen die Sammlungs Maske für das Server Silo abgerufen.
ms.assetid: 1D6434FD-D7BD-45F9-B7C3-238890AF9928
title: Rtlgetsuitemask-Funktion (ntddk. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlGetSuiteMask
api_type:
- DllExport
api_location:
- ntdll.dll
ms.openlocfilehash: ed8d8906273d18125131251636bc6199d166547b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106356915"
---
# <a name="rtlgetsuitemask-function"></a>Rtlgetsuitemask-Funktion

\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können. Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]

Ruft eine Bitmaske ab, die die im System verfügbaren Produkt Suites identifiziert. Wenn diese Funktion in einer Anwendung aufgerufen wird, die im Kontext eines Server Silos ausgeführt wird, wird stattdessen die Sammlungs Maske für das Server Silo abgerufen.

## <a name="syntax"></a>Syntax


```C++
ULONG NTAPI RtlGetSuiteMask(void);
```



## <a name="parameters"></a>Parameter

Diese Funktion besitzt keine Parameter.

## <a name="return-value"></a>Rückgabewert

Eine Bitmaske, die die im System verfügbaren Produkt Suites identifiziert. Die Bitmaske kann die folgenden Werte enthalten.



| Rückgabewert                                                                          | BESCHREIBUNG                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0x00000001</dt> </dl> | Microsoft Small Business Server wurde auf dem System installiert, kann jedoch auf eine andere Version von Windows aktualisiert werden. Weitere Informationen zu diesem Bitflag finden Sie im Abschnitt "Hinweise".<br/>                                           |
| <dl> <dt>0x00000002</dt> </dl> | Windows 10 Enterprise, Windows 8.1 Enterprise, Windows Server 2008 Enterprise, Windows Server 2003, Enterprise Edition oder Windows 2000 Advanced Server ist installiert. Weitere Informationen zu diesem Bitflag finden Sie im Abschnitt "Hinweise".<br/> |
| <dl> <dt>0x00000004</dt> </dl> | Microsoft BackOffice-Komponenten werden installiert.<br/>                                                                                                                                                                                               |
| <dl> <dt>0x00000008</dt> </dl> | Communications Server 2003, Communications Server 2005, Communications Server 2007 oder Communications Server 2007 R2 ist installiert.<br/>                                                                                                           |
| <dl> <dt>0x00000010</dt> </dl> | Terminal Dienste sind installiert. Dieser Wert ist immer festgelegt.<br/> Wenn **Terminalserver** festgelegt ist, aber **singleuserts** nicht festgelegt ist, wird das System im Anwendungsserver Modus ausgeführt.<br/>                                                         |
| <dl> <dt>0x00000020</dt> </dl> | Microsoft Small Business Server wird mit der eingeschränkten Client Lizenz in Kraft installiert. Weitere Informationen zu diesem Bitflag finden Sie im Abschnitt "Hinweise".<br/>                                                                            |
| <dl> <dt>0x00000040</dt> </dl> | Windows XP Embedded ist installiert.<br/>                                                                                                                                                                                                            |
| <dl> <dt>0x00000080</dt> </dl> | Windows Server 2008 Datacenter, Windows Server 2003, Datacenter Edition oder Windows 2000 Datacenter Server ist installiert.<br/>                                                                                                                     |
| <dl> <dt>0x00000100</dt> </dl> | Remotedesktop wird unterstützt, es wird jedoch nur eine interaktive Sitzung unterstützt. Dieser Wert wird festgelegt, es sei denn, das System wird im Anwendungsserver Modus ausgeführt.<br/>                                                                                       |
| <dl> <dt>0x00000200</dt> </dl> | Windows Vista Home Premium, Windows Vista Home Basic oder Windows XP Home Edition ist installiert.<br/>                                                                                                                                               |
| <dl> <dt>0x00000400</dt> </dl> | Windows Server 2003, Web Edition ist installiert.<br/>                                                                                                                                                                                               |
| <dl> <dt>0x00002000</dt> </dl> | Windows Storage Server 2003 R2 oder Windows Storage Server 2003 ist installiert.<br/>                                                                                                                                                                  |
| <dl> <dt>0x00004000</dt> </dl> | Windows Server 2003, Compute Cluster Edition ist installiert.<br/>                                                                                                                                                                                   |
| <dl> <dt>0x00008000</dt> </dl> | Windows Home Server ist installiert.<br/>                                                                                                                                                                                                            |



 

## <a name="remarks"></a>Bemerkungen

Sie sollten nicht nur auf das 0x00000001-Flag zurückgreifen, um zu bestimmen, ob Small Business Server auf dem System installiert ist, da sowohl dieses Flag als auch das 0x00000020-Flag festgelegt werden, wenn diese Produktsuite installiert wird. Wenn Sie diese Installation auf Windows Server Standard Edition upgraden, wird das 0x00000020-Flag nicht gelöscht, aber das 0x00000001-Flag bleibt festgelegt. In diesem Fall ist dies ein Hinweis darauf, dass Small Business Server auf diesem System installiert war. Wenn diese Installation ein weiteres Upgrade auf Windows Server Enterprise Edition durchführt, bleibt das Flag 0x00000001 festgelegt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 10 \[ -Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2016 \[ -Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Ntddk. h</dt> </dl>   |
| Bibliothek<br/>                  | <dl> <dt>Ntdll. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ntdll.dll</dt> </dl> |



 

 




