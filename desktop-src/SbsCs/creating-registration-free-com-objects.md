---
description: Mithilfe von Aktivierungs Kontexten können COM-Objekte verwendet werden, ohne dass Sie registriert werden müssen.
ms.assetid: e6ec7b8b-8032-4dff-8f96-07ae3ffc286d
title: Erstellen Registration-Free COM-Objekten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70e377a04f44e6624294116b8274a8dcc1e82b8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362545"
---
# <a name="creating-registration-free-com-objects"></a>Erstellen Registration-Free COM-Objekten

Mithilfe von Aktivierungs Kontexten können COM-Objekte verwendet werden, ohne dass Sie registriert werden müssen. Dadurch kann Ihre Anwendung mehrere Komponenten mit unterschiedlichen Funktionen aufweisen, die auf Ihrer Version basieren, anstatt deren Registrierungsinformationen. Mehrere Komponenten können dasselbe com-Objekt mit derselben GUID verfügbar machen, haben jedoch unterschiedliche Funktionen, die auf der Version basieren.

Wenn eine Anwendung eine GUID von [**CLSIDFromProgID**](/windows/win32/api/combaseapi/nf-combaseapi-clsidfromprogid)anfordert, sucht com zuerst im aktiven Aktivierungs Kontext nach der Zuordnung von ProgID zu CLSID. Wenn eine Anwendung mithilfe von [**cokreateinstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) einen Instanz-Schnittstellen Zeiger erhält, sucht com im aktiven Aktivierungs Kontext nach der dll, die die CLSID hostet. Wenn der Aktivierungs Kontext die erforderlichen Informationen nicht enthält, sucht com mithilfe der üblichen Methode nach den Informationen in der Registrierung.

Beachten Sie, dass com den Aktivierungs Kontext des erstellenden Threads auf den Hostthread marshallst, da der Aktivierungs Kontext Thread bezogen ist, bevor [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) oder [**DllGetClassObject**](/windows/win32/api/combaseapi/nf-combaseapi-dllgetclassobject) auf dem Hostthread aufgerufen wird. Diese Funktionalität ist in Windows bereits vorhanden, und der Client Code ist nicht erforderlich, um dies zu implementieren.

COM-Klassen können von gehosteten Komponenten exportiert werden, ohne die Registrierung durchlaufen zu müssen. Mehrere Komponenten können dieselbe ProgID für verschiedene com-Objekte verfügbar machen, und ihre Hostinganwendung sollte nur den richtigen Aktivierungs Kontext finden und dann [**CLSIDFromProgID**](/windows/win32/api/combaseapi/nf-combaseapi-clsidfromprogid) und [**cokreateinstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) verwenden, um die Schnittstellen Zeiger des gehosteten Objekts zu erhalten.

 

 
