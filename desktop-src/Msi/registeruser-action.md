---
description: Die Aktion RegisterUser registriert die Benutzerinformationen beim Installationsprogramm, um den Benutzer eines Produkts zu identifizieren.
ms.assetid: da615cb4-d36d-4180-8f97-c9f83c0df1c6
title: RegisterUser-Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f89d43d18839e806939b7a084d37840b9895fdc81efb79fc03867eebe4c5c57
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118626715"
---
# <a name="registeruser-action"></a>RegisterUser-Aktion

Die Aktion RegisterUser registriert die Benutzerinformationen beim Installationsprogramm, um den Benutzer eines Produkts zu identifizieren.

## <a name="sequence-restrictions"></a>Sequenzeinschränkungen

Es gibt keine Sequenzeinschränkungen.

## <a name="actiondata-messages"></a>ActionData-Meldungen



| Feld | Beschreibung der Aktionsdaten   |
|-------|------------------------------|
| \[1\] | Registrierte Benutzerinformationen. |



 

## <a name="remarks"></a>Hinweise

Die Aktion RegisterUser wird während einer Administratorinstallation nicht ausgeführt. Wenn der vom Benutzer eingegebene Produktbezeichner nicht durch die [ValidateProductID-Aktion](validateproductid-action.md)überprüft wurde, wird die [**ProductID-Eigenschaft**](productid.md) nicht festgelegt, und diese Aktion führt nichts aus.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Nutzername**](username.md)
</dt> <dt>

[**Companyname**](companyname.md)
</dt> <dt>

[**Productid**](productid.md)
</dt> </dl>

 

 



