---
title: Zurückgeben von Fehlerinformationen
description: Zurückgeben von Fehlerinformationen
ms.assetid: 4206f2e5-db01-458c-93cb-10c5cd4a4536
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 303db82dc220d09d4db7f52bf4c04ad1e5ca691f
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104391042"
---
# <a name="returning-error-information"></a>Zurückgeben von Fehlerinformationen

Mithilfe der com-Fehler Behandlungs Schnittstellen und-Funktionen können Sie Fehlerinformationen zurückgeben, indem Sie die folgenden Schritte ausführen:

1.  Implementieren Sie die [**ISupportErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-isupporterrorinfo) -Schnittstelle.
2.  Um eine Instanz des generischen Fehler Objekts zu erstellen, rufen Sie [**die Funktion "**](/windows/win32/api/oleauto/nf-oleauto-createerrorinfo) -Funktion" auf.
3.  Um den Inhalt festzulegen, verwenden Sie die [**ikreateerrorinfo**](/windows/win32/api/oaidl/nn-oaidl-icreateerrorinfo) -Methoden.
4.  Um das Fehler Objekt dem aktuellen logischen Thread zuzuordnen, wenden Sie die [**SetErrorInfo**](/windows/win32/api/oleauto/nf-oleauto-seterrorinfo) -Funktion an.

Die Fehler Behandlungs Schnittstellen erstellen und verwalten ein Fehler Objekt, das Informationen über den Fehler enthält. Das Fehler Objekt ist nicht mit dem Objekt identisch, bei dem der Fehler aufgetreten ist. Dabei handelt es sich um ein separates-Objekt, das dem aktuellen Ausführungs Thread zugeordnet ist.

 

 