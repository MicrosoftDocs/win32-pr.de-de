---
title: Abrufen von Fehlerinformationen
description: Abrufen von Fehlerinformationen
ms.assetid: 51a0e401-43f2-4738-9799-a96e2580a29f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e26844505b7c5de3e39c3199a6087c94f35bed9f64ef11a65d1c6df9a3dd4e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118309652"
---
# <a name="retrieving-error-information"></a>Abrufen von Fehlerinformationen

Mithilfe der COM-Fehlerbehandlungsschnittstellen und -funktionen können Sie Fehlerinformationen wie folgt abrufen:

1.  Überprüfen Sie, ob der zurückgegebene Wert einen Fehler darstellt, den das Objekt behandeln kann.
2.  Rufen Sie [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) auf, um einen Zeiger auf die [**ISupportErrorInfo-Schnittstelle**](/windows/win32/api/oaidl/nn-oaidl-isupporterrorinfo) abzurufen. Rufen Sie dann [**ISupportErrorInfo::InterfaceSupportsErrorInfo**](/windows/win32/api/oaidl/nf-oaidl-isupporterrorinfo-interfacesupportserrorinfo) auf, um zu überprüfen, ob der Fehler von dem Objekt ausgelöst wurde, das ihn zurückgegeben hat, und ob das Fehlerobjekt den aktuellen Fehler und nicht einen vorherigen Aufruf betrifft.
3.  Rufen Sie die [**GetErrorInfo-Funktion**](/windows/win32/api/oleauto/nf-oleauto-geterrorinfo) auf, um einen Zeiger auf das Fehlerobjekt abzurufen.
4.  Verwenden Sie zum Abrufen von Informationen aus dem Fehlerobjekt die [**IErrorInfo-Methoden.**](/windows/win32/api/oaidl/nn-oaidl-ierrorinfo)

Wenn das Objekt nicht bereit ist, den Fehler zu behandeln, aber die Fehlerinformationen weiter unten in der Aufrufkette weitergeben muss, sollte es einfach den Rückgabewert an seinen Aufrufer übergeben. Da die [**GetErrorInfo-Funktion**](/windows/win32/api/oleauto/nf-oleauto-geterrorinfo) die Fehlerinformationen löscht und den Besitz des Fehlerobjekts an den Aufrufer übergibt, sollte die Funktion nur von dem Objekt aufgerufen werden, das den Fehler behandelt.

 

 