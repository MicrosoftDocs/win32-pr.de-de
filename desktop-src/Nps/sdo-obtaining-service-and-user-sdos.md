---
title: Abrufen von Dienst- und Benutzer-SDOs
description: Um SDOs für NPS (IAS) oder einen bestimmten Benutzer zu erhalten, rufen Sie die Methoden ISdoMachine GetServiceSDO oder ISdoMachine GetUserSDO auf.
ms.assetid: 23e23fb3-0102-4c36-b30f-18604131ee32
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aebef1e695236bd1449ab886cb998a67f09c2cafc8ded446b0b7e1ad89b01181
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120128590"
---
# <a name="obtaining-service-and-user-sdos"></a>Abrufen von Dienst- und Benutzer-SDOs

> [!Note]  
> Internet Authentication Service (IAS) wurde ab Windows Server 2008 in Network Policy Server (NPS) umbenannt.

 

Um SDOs für NPS (IAS) oder einen bestimmten Benutzer zu erhalten, rufen Sie die [**Methoden ISdoMachine::GetServiceSDO**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getservicesdo) oder [**ISdoMachine::GetUserSDO**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getusersdo) auf. Diese Methoden geben Zeiger auf [**IUnknown-Schnittstellen**](/windows/win32/api/unknwn/nn-unknwn-iunknown) für diese Objekte zurück. Verwenden Sie für den Benutzer-SDO die [**IUnknown::QueryInterface-Methode,**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) um eine [**ISdo-Schnittstelle**](/windows/desktop/api/sdoias/nn-sdoias-isdo) für das Objekt zu erhalten. Verwenden Sie für den Dienst-SDO **IUnknown::QueryInterface,** um eine [**ISdo-Schnittstelle**](/windows/desktop/api/sdoias/nn-sdoias-isdo) oder [**eine ISdoServiceControl-Schnittstelle zu**](/windows/desktop/api/sdoias/nn-sdoias-isdoservicecontrol) erhalten.

Rufen Sie vor dem Aufrufen von [**ISdoMachine::GetServiceSDO**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getservicesdo) oder [**ISdoMachine::GetUserSDO**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getusersdo) [**ISdoMachine::Attach**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-attach) auf, um das Computerobjekt dem lokalen Computer zu zuordnen.

Beispielcode zum Abrufen dieser SDOs finden Sie unter Abrufen eines [Dienst-SDO](/windows/desktop/Nps/sdo-retrieving-a-service-sdo) und Abrufen eines [Benutzer-SDO.](/windows/desktop/Nps/sdo-retrieving-a-user-sdo)

 

 