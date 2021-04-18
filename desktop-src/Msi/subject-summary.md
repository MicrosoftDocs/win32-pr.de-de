---
description: Der Wert der Eigenschaft "betreffzusammenfassung" überträgt den Namen des Produkts, der Transformation oder des Patches, das vom Paket installiert wird.
ms.assetid: fb08a240-db30-477f-8dc0-701156d73cfc
title: Subject Summary-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d21139f686bc8a6cfc5ba2edecdfc57c349d84ef
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364920"
---
# <a name="subject-summary-property"></a>Subject Summary-Eigenschaft

Der Wert der Eigenschaft " **betreffzusammenfassung** " überträgt den Namen des Produkts, der Transformation oder des Patches, das vom Paket installiert wird.

Es liegt an der Erstellung einer Installations Datenbank, einer Transformation oder eines Patchpakets, um den Wert dieser Eigenschaft in den Zusammenfassungs Informationen bereitzustellen. Autoren sollten die folgenden Schritte ausführen, um den richtigen Wert zu bestimmen.

-   Legen Sie die Eigenschaft für die **betreffzusammenfassung** in einem Installationspaket auf denselben Wert fest wie die [**ProductName**](productname.md) -Eigenschaft.
-   Legen Sie die Eigenschaft für die **betreffzusammenfassung** in einer Transformation auf denselben Wert wie die Eigenschaft für die **betreffzusammenfassung** im ursprünglichen Installationspaket fest.
-   Legen Sie die Eigenschaft für die **betreffzusammenfassung** in den Zusammenfassungs Informationen eines Patchpakets auf eine kurze Beschreibung des Patches fest, der den Namen des Produkts enthält.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer unter Windows Server 2003 oder Windows XP<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Patchnewsummarysubject**](patchnewsummarysubject.md)
</dt> <dt>

[Beschreibungen der Zusammenfassungs Eigenschaften](summary-property-descriptions.md)
</dt> </dl>

 

 




