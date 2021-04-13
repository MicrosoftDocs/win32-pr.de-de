---
title: Abrufen von Dienst-und Benutzer-SDOs
description: Rufen Sie zum Abrufen von SDOs für NPS (IAS) oder einen bestimmten Benutzer die isdomachine getservicesdo-Methode oder die isdomachine getusersdo-Methode auf.
ms.assetid: 23e23fb3-0102-4c36-b30f-18604131ee32
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c7562c3b7c6aa1150ba3ce6581441064eb386f7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315711"
---
# <a name="obtaining-service-and-user-sdos"></a>Abrufen von Dienst-und Benutzer-SDOs

> [!Note]  
> Der Internet Authentifizierungsdienst (IAS) wurde ab Windows Server 2008 in den Netzwerk Richtlinien Server (Network Policy Server, NPS) umbenannt.

 

Rufen Sie zum Abrufen von SDOs für NPS (IAS) oder einen bestimmten Benutzer die [**isdomachine:: getservicesdo**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getservicesdo) -Methode oder die [**isdomachine:: getusersdo**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getusersdo) -Methode auf. Diese Methoden geben Zeiger auf [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstellen für diese Objekte zurück. Verwenden Sie für den Benutzer SDO die [**IUnknown:: QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) -Methode, um eine [**isdo**](/windows/desktop/api/sdoias/nn-sdoias-isdo) -Schnittstelle für das Objekt abzurufen. Verwenden Sie für den Dienst SDO **IUnknown:: QueryInterface** , um eine [**isdo**](/windows/desktop/api/sdoias/nn-sdoias-isdo) -Schnittstelle oder eine [**isdoservicecontrol**](/windows/desktop/api/sdoias/nn-sdoias-isdoservicecontrol) -Schnittstelle zu erhalten.

Rufen Sie vor dem Aufrufen von [**isdomachine:: getservicesdo**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getservicesdo) oder [**isdomachine:: getusersdo**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getusersdo) [**isdomachine:: Attach**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-attach) auf, um das Computer Objekt dem lokalen Computer zuzuordnen.

Informationen zum Abrufen dieser SDOs finden Sie unter [Abrufen eines SDO-diensdo](/windows/desktop/Nps/sdo-retrieving-a-service-sdo) und [Abrufen eines Benutzers SDO (SDO](/windows/desktop/Nps/sdo-retrieving-a-user-sdo) ).

 

 