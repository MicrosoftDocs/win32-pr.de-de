---
title: Routing Protokoll Schnittstellen-Funktionen
description: Implementieren Sie die folgenden Funktionen für eine Routing Protokoll-dll.
ms.assetid: fd780458-ef23-4ef2-8fe8-29b32100917f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b696d516cf0fc0b13d66fdc53b384a28fac8696a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103949072"
---
# <a name="routing-protocol-interface-functions"></a>Routing Protokoll Schnittstellen-Funktionen

Implementieren Sie die folgenden Funktionen für eine Routing Protokoll-dll:

[**AddInterface**](/windows/desktop/api/Routprot/nc-routprot-padd_interface)

[**Connectclient**](/windows/desktop/api/Routprot/nc-routprot-pconnect_client)

[**Delta Info**](/windows/desktop/api/Routprot/nc-routprot-pdelete_interface)

[**Disconnectclient**](/windows/desktop/api/Routprot/nc-routprot-pdisconnect_client)

[**Doupdateroutes**](/windows/desktop/api/Routprot/nc-routprot-pdo_update_routes)

[*"Doupdateservices"*](/previous-versions/windows/desktop/legacy/aa374005(v=vs.85))

[**Geteventmessage**](/windows/desktop/api/Routprot/nc-routprot-pget_event_message)

[**GetGlobalInfo**](/windows/desktop/api/Routprot/nc-routprot-pget_global_info)

[**Getinterfacetten Info**](/windows/desktop/api/Routprot/nc-routprot-pget_interface_info)

[**Getmfestatus**](/windows/desktop/api/Routprot/nc-routprot-pget_mfe_status)

[**GetNeighbors**](/windows/desktop/api/Routprot/nc-routprot-pget_neighbors)

[**Interfacestatus**](/windows/desktop/api/Routprot/nc-routprot-pinterface_status)

[**Mibcreate**](/windows/desktop/api/Routprot/nc-routprot-pmib_create)

[**Mibdelete**](/windows/desktop/api/Routprot/nc-routprot-pmib_delete)

[**Mibget**](/windows/desktop/api/Routprot/nc-routprot-pmib_get)

[**Mibgetfirst**](/windows/desktop/api/Routprot/nc-routprot-pmib_get_first)

[**Mibgetnext**](/windows/desktop/api/Routprot/nc-routprot-pmib_get_next)

[*Mibgettrapinfo*](/windows/desktop/api/Routprot/nc-routprot-pmib_get_trap_info)

[**Mibset**](/windows/desktop/api/Routprot/nc-routprot-pmib_set)

[**Mibsettrapinfo**](/windows/desktop/api/Routprot/nc-routprot-pmib_set_trap_info)

[**Querypower**](/windows/desktop/api/Routprot/nc-routprot-pquery_power)

[**Register Protocol**](/windows/desktop/api/Routprot/nc-routprot-pregister_protocol)

[**Setglobalinfo**](/windows/desktop/api/Routprot/nc-routprot-pset_global_info)

[**Setinterfacetten Info**](/windows/desktop/api/Routprot/nc-routprot-pset_interface_info)

[**SetPower**](/windows/desktop/api/Routprot/nc-routprot-pset_power)

[**Startcomplete**](/windows/desktop/api/Routprot/nc-routprot-pstart_complete)

[**Startprotokoll**](/windows/desktop/api/Routprot/nc-routprot-pstart_protocol)

[**Stop Protocol**](/windows/desktop/api/Routprot/nc-routprot-pstop_protocol)

[**Unbindinterface**](/previous-versions/windows/desktop/legacy/aa382296(v=vs.85))

Wenn das Routing Protokoll die Dienst Verarbeitung unterstützt, implementieren Sie zusätzlich zu den oben aufgeführten die folgenden Funktionen:

[**"Doupdateservices"**](/previous-versions/windows/desktop/legacy/aa374005(v=vs.85))

 

 