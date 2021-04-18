---
description: Registrierung und Laden von schattenkopieanbietern
ms.assetid: f9bb72ce-9a2b-43cd-9697-1f6598a46e3e
title: Registrierung und Laden von schattenkopieanbietern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 725613ff37450075c964b3c66fce3ffba1a70529
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344999"
---
# <a name="shadow-copy-provider-registration-and-loading"></a>Registrierung und Laden von schattenkopieanbietern

## <a name="provider-registration"></a>Anbieter Registrierung

Nur VSS ruft Anbieter auf. Der Anbieter registriert sich für Aufrufe durch Aufrufen von [**ivssadmin:: RegisterProvider**](/windows/desktop/api/VsAdmin/nf-vsadmin-ivssadmin-registerprovider)und übergibt **VSS \_ Prov \_ Hardware** für den *eprovidertype* -Parameter. Nach der Registrierung wird der Anbieter an der Schattenkopieverwaltung beteiligt sein, bis die Registrierung mithilfe von [**ivssadmin:: unregisterprovider**](/windows/desktop/api/VsAdmin/nf-vsadmin-ivssadmin-unregisterprovider)aufgehoben wird.

## <a name="provider-loading-and-unloading"></a>Laden und Entladen von Anbietern

Anbieter können häufig geladen und entladen werden. Anbieter können [**ivssproviderbenachrichtigungen**](/windows/desktop/api/VsProv/nn-vsprov-ivssprovidernotifications) implementieren, um zu bestimmen, wann der Anbieter von VSS geladen oder entladen wird.

 

 



