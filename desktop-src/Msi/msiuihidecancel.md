---
description: Diese Windows Installer-Eigenschaft gibt an, wann die interne Benutzeroberflächesebene festgelegt wurde, um die Schaltfläche "Abbrechen" auszublenden.
ms.assetid: 0e842bee-32c2-41ae-97f3-bc8b34960a44
title: MsiUIHideCancel-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6da3c0888ea760e7e8627710b061112d350f94af569697b7ad0616d1dbacbbf0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118943988"
---
# <a name="msiuihidecancel-property"></a>MsiUIHideCancel-Eigenschaft

Das Installationsprogramm legt die **MsiUIHideCancel-Eigenschaft** auf 1 fest, wenn die interne Benutzeroberflächesebene so festgelegt wurde, dass INSTALLUILEVEL \_ HIDECANCEL mit der [**MsiSetInternalUI-Funktion**](/windows/desktop/api/Msi/nf-msi-msisetinternalui) oder der [UILevel-Eigenschaft](installer-uilevel.md)des [**Installer-Objekts**](installer-object.md) oder mithilfe von [Befehlszeilenoptionen](command-line-options.md)eingeschlossen wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installationsprogramm 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installationsprogramm 3.0 oder höher auf Windows Server 2003 oder Windows XP. Informationen zu den mindestens erforderlichen Windows Service Packs, die für eine Windows Installer-Version erforderlich sind, finden Sie unter Run-Time [Anforderungen](windows-installer-portal.md) für Windows Installer.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften](properties.md)
</dt> <dt>

[Nicht unterstützt in Windows Installer 2.0 und früher](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




