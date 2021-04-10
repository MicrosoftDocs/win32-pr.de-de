---
title: Abrufen von Fehlerinformationen
description: Abrufen von Fehlerinformationen
ms.assetid: 51a0e401-43f2-4738-9799-a96e2580a29f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6a5918ee7338d1b8428079da20ecb43c7b4b4ef
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104039637"
---
# <a name="retrieving-error-information"></a>Abrufen von Fehlerinformationen

Mithilfe der Schnittstellen und Funktionen für die com-Fehlerbehandlung können Sie Fehlerinformationen wie folgt abrufen:

1.  Überprüfen Sie, ob der zurückgegebene Wert einen Fehler darstellt, der vom-Objekt verarbeitet werden soll.
2.  Ruft [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) auf, um einen Zeiger auf die [**ISupportErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-isupporterrorinfo) -Schnittstelle zu erhalten. Anschließend wird [**ISupportErrorInfo:: interfakesupportserrorinfo**](/windows/win32/api/oaidl/nf-oaidl-isupporterrorinfo-interfacesupportserrorinfo) aufgerufen, um zu überprüfen, ob der Fehler von dem zurückgegebenen Objekt ausgelöst wurde und dass sich das Fehler Objekt auf den aktuellen Fehler und nicht auf einen vorherigen-Befehl bezieht.
3.  Um einen Zeiger auf das Fehler Objekt zu erhalten, müssen Sie die [**GetErrorInfo**](/windows/win32/api/oleauto/nf-oleauto-geterrorinfo) -Funktion aufrufen.
4.  Verwenden Sie zum Abrufen von Informationen aus dem Fehler Objekt die [**IErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-ierrorinfo) -Methoden.

Wenn das Objekt nicht für die Behandlung des Fehlers vorbereitet ist, aber die Fehlerinformationen weiter unten in der Aufruf Kette weitergeben muss, sollte der Rückgabewert einfach an seinen Aufrufer übergeben werden. Da die [**GetErrorInfo**](/windows/win32/api/oleauto/nf-oleauto-geterrorinfo) -Funktion die Fehlerinformationen löscht und den Besitz des Error-Objekts an den Aufrufer übergibt, sollte die Funktion nur von dem Objekt aufgerufen werden, das den Fehler behandelt.

 

 