---
description: Wenn die LIMITUI-Eigenschaft festgelegt ist, ist die Beim Installieren des Pakets verwendete Benutzeroberflächenebene auf Basic beschränkt.
ms.assetid: 1a75e66b-958a-4fa8-b13c-ced976c9508e
title: LIMITUI-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 969b6e1c1de5a55581fa8d24f6d538c829e18fb48afb9bdc2fd04bae69c15162
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119013138"
---
# <a name="limitui-property"></a>LIMITUI-Eigenschaft

Wenn die **LIMITUI-Eigenschaft** festgelegt ist, ist die Beim Installieren des Pakets verwendete Benutzeroberflächenebene auf Basic beschränkt. Diese Eigenschaft ist in Paketen erforderlich, die keine erstellte Benutzeroberfläche haben, aber weiterhin Ui-Tabellen wie die [Dialogtabelle](dialog-table.md)enthalten. Eine Beschreibung der Benutzeroberflächenebenen finden Sie unter [ **MsiSetInternalUI.**](/windows/desktop/api/Msi/nf-msi-msisetinternalui)

## <a name="remarks"></a>Hinweise

Installationspakete, die die **LIMITUI-Eigenschaft** enthalten, müssen auch die [**Eigenschaft ARPNOMODIFY**](arpnomodify.md) enthalten. Dies ist erforderlich, damit ein Benutzer beim Versuch, ein Produkt zu konfigurieren, das richtige Verhalten aus dem Hilfsprogramm **Software** im **Systemsteuerung** abrufen kann.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installationsprogramm 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installationsprogramm auf Windows Server 2003 oder Windows XP. Informationen zu den Windows Service [Pack-Mindestanforderungen,](windows-installer-portal.md) die für eine Windows Installer-Version erforderlich sind, finden Sie unter Run-Time Anforderungen für Windows Installer.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften](properties.md)
</dt> <dt>

[**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui)
</dt> <dt>

[**ARPNOMODIFY**](arpnomodify.md)
</dt> </dl>

 

 




