---
title: Die IADs und IDirectoryObject-Schnittstellen
description: ADSI-Clients verwalten und bearbeiten Verzeichnisdienstobjekte mithilfe einer von zwei COM-Schnittstellen-IADs oder IDirectoryObject.
ms.assetid: f9c486b0-3dfb-4abf-afbf-08749e04315f
ms.tgt_platform: multiple
keywords:
- IADs ADSI , Informationen
- IDirectoryObject ADSI , Informationen
- ADSI ADSI ,using-, IADs- und IDirectoryObject-Schnittstellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6dccfa643c0076224abece6f449f20caf5a4de5d378c03d37cf0e2248ed5a50b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117838380"
---
# <a name="the-iads-and-idirectoryobject-interfaces"></a>Die IADs und IDirectoryObject-Schnittstellen

ADSI-Clients verwalten und bearbeiten Verzeichnisdienstobjekte mithilfe einer von zwei COM-Schnittstellen: [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) oder [**IDirectoryObject.**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) **IADs** sind eine [**IDispatch-Schnittstelle,**](/windows/win32/api/oaidl/nn-oaidl-idispatch) die für die Verwendung durch spät gebundene Clients vorgesehen ist, z. B. clients, die in Microsoft Visual Basic, Java und verschiedenen Skriptsprachen geschrieben wurden. **IDirectoryObject** ist eine vtable-Schnittstelle, die direkten Zugriff auf Objekte durch früh gebundene Clients ermöglicht, z. B. solche, die in C und C++ geschrieben sind.

Jedes ADSI-Objekt muss sowohl [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) als auch [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject)implementieren. ADSI-Clients, die in Sprachen wie C oder C++ geschrieben sind und direkt auf VTables zugreifen können, können beide Schnittstellen verwenden, jedoch nicht beide in derselben Anwendung. ADSI-Clients, die in Visual Basic oder Java geschrieben wurden, sind auf die Verwendung von **IADs** beschränkt.

Mit der [**IADs-Schnittstelle**](/windows/desktop/api/Iads/nn-iads-iads) können spät gebundene Clients die inhärenten Housekeeping-Features des ADSI-Objektmodells nutzen. Zu diesen Features gehört der Eigenschaftencache, mit dem Clients Eigenschaften lesen und schreiben können, ohne für jeden Aufruf über die Leitung zu gehen. Darüber hinaus profitieren Clientanwendungen von leistungsstarken Benutzeroberflächen- und ActiveX-Steuerelementbibliotheken und einem einfacheren Programmierstil. Im Gegenzug müssen spät gebundene Clients den **VARIANT-Datentyp** verwenden, was die Verwendung der umfangreicheren nativen Datentypen ausschließt, die von ADSI bereitgestellt werden.

Die [**IDirectoryObject-Schnittstelle**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) ermöglicht es früh gebundenen Clients, die nativen Verzeichnisdienstdatentypen vollständig zu nutzen, um einen geringfügigen Leistungsvorteil durch die Verwendung des Eigenschaftencaches zu erzielen. Im Gegenzug ermöglicht die **IDirectoryObject-Schnittstelle** direkten Direktenzugriff auf Objekteigenschaften über eine einzelne Anforderung und nicht über einzelne **Get-** und Put-Aufrufe. 

 

 