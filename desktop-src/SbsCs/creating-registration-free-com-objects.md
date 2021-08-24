---
description: Aktivierungskontexte ermöglichen die Verwendung von COM-Objekten, ohne dass sie registriert werden müssen.
ms.assetid: e6ec7b8b-8032-4dff-8f96-07ae3ffc286d
title: Erstellen Registration-Free COM-Objekten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 263d5a6c8160eaf15eba4eb799123e0e79d126ccd94b1d4a7a6d332bdb27dd51
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119142363"
---
# <a name="creating-registration-free-com-objects"></a>Erstellen Registration-Free COM-Objekten

Aktivierungskontexte ermöglichen die Verwendung von COM-Objekten, ohne dass sie registriert werden müssen. Dadurch kann Ihre Anwendung über mehrere Komponenten mit unterschiedlichen Funktionen verfügen, die auf ihrer Version und nicht auf ihren Registrierungsinformationen basieren. Mehrere Komponenten können dasselbe COM-Objekt mit der gleichen GUID verfügbar machen, verfügen jedoch je nach Version über unterschiedliche Funktionen.

Wenn eine Anwendung eine GUID von [**CLSIDFromProgID**](/windows/win32/api/combaseapi/nf-combaseapi-clsidfromprogid)an fordert, sucht COM zuerst im aktiven Aktivierungskontext nach der Zuordnung von progid zu CLSID. Wenn eine Anwendung [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) verwendet, um einen Instanzschnittstellenzeiger zu erhalten, durchsucht COM im aktiven Aktivierungskontext, um zu finden, welche DLL die CLSID hosten wird. Wenn der Aktivierungskontext nicht die erforderlichen Informationen enthält, sucht COM mithilfe der üblichen Methode nach den Informationen in der Registrierung.

Beachten Sie, dass COM den Aktivierungskontext des erstellenden Threads an den Hostthread marshallt und aktiviert, bevor [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) oder [**DllGetClassObject**](/windows/win32/api/combaseapi/nf-combaseapi-dllgetclassobject) im Hostthread aufgerufen wird, da Aktivierungskontexte pro Thread verwendet werden. Diese Funktionalität ist bereits in der Windows, client code is not required to doanything to implement this.

COM-Klassen können von gehosteten Komponenten exportiert werden, ohne die Registrierung zu verwenden. Mehrere Komponenten können dieselbe ProgID für verschiedene COM-Objekte verfügbar machen, und Ihre Hostinganwendung sollte nur den richtigen Aktivierungskontext finden und [**dann CLSIDFromProgID**](/windows/win32/api/combaseapi/nf-combaseapi-clsidfromprogid) und [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) verwenden, um die Schnittstellenzeder des gehosteten Objekts zu erhalten.

 

 
