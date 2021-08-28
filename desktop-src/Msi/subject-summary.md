---
description: Der Wert der Eigenschaft Betreffzusammenfassung gibt den Namen des Produkts, der Transformation oder des Patches an, das bzw. der vom Paket installiert wird.
ms.assetid: fb08a240-db30-477f-8dc0-701156d73cfc
title: Eigenschaft "Zusammenfassung des Betreffs"
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad9d92328f142e4fd47567e92d4fe3bb7f016b0bf058b2932f7e1136687507e8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119627230"
---
# <a name="subject-summary-property"></a>Eigenschaft "Zusammenfassung des Betreffs"

Der Wert der **Eigenschaft Betreffzusammenfassung** gibt den Namen des Produkts, der Transformation oder des Patches an, das bzw. der vom Paket installiert wird.

Der Autor eines Installationsdatenbank-, Transformations- oder Patchpakets muss den Wert dieser Eigenschaft in den Zusammenfassungsinformationen bereitstellen. Autoren sollten folgende Schritte unternehmen, um den richtigen Wert zu ermitteln.

-   Legen Sie **die Eigenschaft Betreffzusammenfassung** in einem Installationspaket auf den gleichen Wert wie die [**ProductName-Eigenschaft**](productname.md) fest.
-   Legen Sie **die Eigenschaft Zusammenfassung des** Betreffs in einer Transformation auf den gleichen Wert wie die Eigenschaft **Betreffzusammenfassung** im ursprünglichen Installationspaket fest.
-   Legen Sie **die Eigenschaft Betreffzusammenfassung** in den Zusammenfassungsinformationen eines Patchpakets auf eine kurze Beschreibung des Patches fest, die den Namen des Produkts enthält.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installationsprogramm auf Windows Server 2003 oder Windows XP<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**PATCH PATCHUMMARYSUBJECT**](patchnewsummarysubject.md)
</dt> <dt>

[Zusammenfassungseigenschaftsbeschreibungen](summary-property-descriptions.md)
</dt> </dl>

 

 




