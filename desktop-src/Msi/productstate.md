---
description: Der Installer legt die Eigenschaft productstate bei der Initialisierung auf den Installationsstatus für das Produkt fest.
ms.assetid: 833e9a15-10f8-4b1c-945f-bc02b506f627
title: Productstate (Eigenschaft)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a51ea88058aa8bae6b67acaea96b506a7560c7a2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364506"
---
# <a name="productstate-property"></a>Productstate (Eigenschaft)

Der Installer legt die Eigenschaft **productstate** bei der Initialisierung auf den Installationsstatus für das Produkt fest. Diese Eigenschaft wird auf einen der folgenden InstallState-Datentypen festgelegt, die von " [**msiqueryproductstate**](/windows/desktop/api/Msi/nf-msi-msiqueryproductstatea)" zurückgegeben werden.



| INSTALLSTATE             | Numerischer Wert | Installationsstatus des Produkts                   |
|--------------------------|---------------|-------------------------------------------------|
| InstallState \_ unbekannt    | -1            | Das Produkt wird weder angekündigt noch installiert. |
| InstallState \_ angekündigt | 1             | Das Produkt wird angekündigt, aber nicht installiert.    |
| InstallState \_ fehlt.     | 2             | Das Produkt wird für einen anderen Benutzer installiert.  |
| InstallState ( \_ Standard)    | 5             | Das Produkt ist für den aktuellen Benutzer installiert.  |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer unter Windows Server 2003 oder Windows XP. Informationen zu den minimalen Windows-Service Pack, die für eine Windows Installer Version erforderlich sind, finden Sie in den [Windows Installer Run-Time Anforderungen](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften](properties.md)
</dt> </dl>

 

 




