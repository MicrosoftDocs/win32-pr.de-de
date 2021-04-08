---
description: Die Aktion RegisterUser registriert die Benutzerinformationen beim Installationsprogramm, um den Benutzer eines Produkts zu identifizieren.
ms.assetid: da615cb4-d36d-4180-8f97-c9f83c0df1c6
title: RegisterUser-Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 686628d29094f951994b072ad4451a383a405965
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756463"
---
# <a name="registeruser-action"></a>RegisterUser-Aktion

Die Aktion RegisterUser registriert die Benutzerinformationen beim Installationsprogramm, um den Benutzer eines Produkts zu identifizieren.

## <a name="sequence-restrictions"></a>Sequenz Einschränkungen

Es gibt keine Sequenz Einschränkungen.

## <a name="actiondata-messages"></a>Aktions Daten Meldungen



| Feld | Beschreibung der Aktions Daten   |
|-------|------------------------------|
| \[1\] | Registrierte Benutzerinformationen. |



 

## <a name="remarks"></a>Bemerkungen

Die Aktion "RegisterUser" wird während einer administrativen Installation nicht durchgeführt. Wenn der vom Benutzer eingegebene Produkt Bezeichner nicht durch die [ValidateProductID-Aktion](validateproductid-action.md)überprüft wurde, ist die [**ProductID-**](productid.md) Eigenschaft nicht festgelegt, und diese Aktion führt keine Aktion aus.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**User**](username.md)
</dt> <dt>

[**CompanyName**](companyname.md)
</dt> <dt>

[**ProductID**](productid.md)
</dt> </dl>

 

 



