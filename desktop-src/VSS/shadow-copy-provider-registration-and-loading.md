---
description: Registrierung und Laden des Schattenkopieanbieters
ms.assetid: f9bb72ce-9a2b-43cd-9697-1f6598a46e3e
title: Registrierung und Laden des Schattenkopieanbieters
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bbb239303884314375ec865e3862d6a65af7de27bd7351a74e92604d06876bb2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118998110"
---
# <a name="shadow-copy-provider-registration-and-loading"></a>Registrierung und Laden des Schattenkopieanbieters

## <a name="provider-registration"></a>Anbieterregistrierung

Nur VSS ruft Anbieter auf. Der Anbieter registriert sich für Aufrufe, indem [**er IVssAdmin::RegisterProvider**](/windows/desktop/api/VsAdmin/nf-vsadmin-ivssadmin-registerprovider)aufruft und **VSS \_ PROV \_ HARDWARE** für den *eProviderType-Parameter* übergibt. Nach der Registrierung ist der Anbieter an der Schattenkopieverwaltung beteiligt, bis die Registrierung mit [**IVssAdmin::UnregisterProvider**](/windows/desktop/api/VsAdmin/nf-vsadmin-ivssadmin-unregisterprovider)aufgehoben wird.

## <a name="provider-loading-and-unloading"></a>Laden und Entladen von Anbietern

Anbieter können häufig geladen und entladen werden. Anbieter können [**IVssProviderNotifications**](/windows/desktop/api/VsProv/nn-vsprov-ivssprovidernotifications) implementieren, um zu bestimmen, wann VSS den Anbieter lädt oder entlädt.

 

 



