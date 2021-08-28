---
title: Zurückgeben von Fehlerinformationen
description: Zurückgeben von Fehlerinformationen
ms.assetid: 4206f2e5-db01-458c-93cb-10c5cd4a4536
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 545c697be7da64362ecce0f5b4c45272832ad682d8b4dd0eb5234620b993e5f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118309642"
---
# <a name="returning-error-information"></a>Zurückgeben von Fehlerinformationen

Mithilfe der COM-Fehlerbehandlungsschnittstellen und -funktionen können Sie Fehlerinformationen zurückgeben, indem Sie die folgenden Schritte ausführen:

1.  Implementieren Sie die [**ISupportErrorInfo-Schnittstelle.**](/windows/win32/api/oaidl/nn-oaidl-isupporterrorinfo)
2.  Um eine Instanz des generischen Fehlerobjekts zu erstellen, rufen Sie die [**CreateErrorInfo-Funktion**](/windows/win32/api/oleauto/nf-oleauto-createerrorinfo) auf.
3.  Verwenden Sie zum Festlegen des Inhalts die [**ICreateErrorInfo-Methoden.**](/windows/win32/api/oaidl/nn-oaidl-icreateerrorinfo)
4.  Um das Fehlerobjekt dem aktuellen logischen Thread zuzuordnen, rufen Sie die [**SetErrorInfo-Funktion**](/windows/win32/api/oleauto/nf-oleauto-seterrorinfo) auf.

Die Fehlerbehandlungsschnittstellen erstellen und verwalten ein Fehlerobjekt, das Informationen zum Fehler bereitstellt. Das Fehlerobjekt ist nicht dasselbe wie das Objekt, bei dem der Fehler aufgetreten ist. Es handelt sich um ein separates Objekt, das dem aktuellen Ausführungsthread zugeordnet ist.

 

 