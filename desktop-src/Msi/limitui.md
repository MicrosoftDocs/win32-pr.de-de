---
description: Wenn die limitui-Eigenschaft festgelegt ist, ist die Benutzeroberflächen Ebene, die bei der Installation des Pakets verwendet wird, auf Basic beschränkt.
ms.assetid: 1a75e66b-958a-4fa8-b13c-ced976c9508e
title: Limitui (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e564e82a2daba4b6d5a91cb05acd74e1efc26c84
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369400"
---
# <a name="limitui-property"></a>Limitui (Eigenschaft)

Wenn die **limitui** -Eigenschaft festgelegt ist, ist die Benutzeroberflächen Ebene, die bei der Installation des Pakets verwendet wird, auf Basic beschränkt. Diese Eigenschaft ist in Paketen erforderlich, die über keine erstellte Benutzeroberfläche verfügen, aber trotzdem Benutzeroberflächen Tabellen wie die [Dialog Feld Tabelle](dialog-table.md)enthalten. Eine Beschreibung der UI-Ebenen finden Sie unter [ **MsiSetInternalUI** .](/windows/desktop/api/Msi/nf-msi-msisetinternalui)

## <a name="remarks"></a>Bemerkungen

Installationspakete, die die **limitui** -Eigenschaft enthalten, müssen auch die [**arpnomodify**](arpnomodify.md) -Eigenschaft enthalten. Dies ist erforderlich, damit ein Benutzer das richtige Verhalten von der **System Steuerungs** Option "Software **" beim Versuch** , ein Produkt zu konfigurieren, erhält.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer unter Windows Server 2003 oder Windows XP. Informationen zu den minimalen Windows-Service Pack, die für eine Windows Installer Version erforderlich sind, finden Sie in den [Windows Installer Run-Time Anforderungen](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften](properties.md)
</dt> <dt>

[**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui)
</dt> <dt>

[**Arpnomodify**](arpnomodify.md)
</dt> </dl>

 

 




