---
description: Die ProductID-Eigenschaft wird nach einer erfolgreichen Validierung auf die vollständige ProductID festgelegt. Dieser Wert wird von der Benutzeroberfläche angezeigt und von der registerproduct-Aktion verwendet. Nach einer erfolgreichen Überprüfung wird diese Eigenschaft von der ValidateProductID-Aktion oder der ValidateProductID ControlEvent festgelegt. Beachten Sie, dass die für die spezielle Beispiel Benutzeroberfläche, die mit dem SDK als Uisample.msi bereitgestellt wird, einen Wert für ProductID erfordert. Wenn Sie diese Benutzeroberfläche verwenden, aber nicht ProductID verwenden möchten, um Produkt Bezeichner zu validieren, legen Sie die ProductID-Eigenschaft auf &\# 0034; None&\# 0034; in der Eigenschaften Tabelle fest.
ms.assetid: 6af23f2d-b22a-470d-b979-da32776e0007
title: ProductID-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6cf616e2bc34ce70deb5f6b63dba7287002d4fb2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352038"
---
# <a name="productid-property"></a>ProductID-Eigenschaft

Die **ProductID** -Eigenschaft wird nach einer erfolgreichen Validierung auf die vollständige **ProductID** festgelegt.

Dieser Wert wird von der Benutzeroberfläche angezeigt und von der [registerproduct-Aktion](registerproduct-action.md)verwendet.

Nach einer erfolgreichen Überprüfung wird diese Eigenschaft von der [ValidateProductID-Aktion](validateproductid-action.md) oder der [ValidateProductID-ControlEvent](validateproductid-controlevent.md)festgelegt.

Beachten Sie, dass die für das SDK als Uisample.msi bereitgestellte Beispiel Benutzeroberfläche einen Wert für **ProductID** erfordert. Wenn Sie diese Benutzeroberfläche verwenden, aber nicht **ProductID** verwenden möchten, um Produkt Bezeichner zu validieren, legen Sie die **ProductID-** Eigenschaft in der [Eigenschaften Tabelle](property-table.md)auf "None" fest.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer unter Windows Server 2003 oder Windows XP. Informationen zu den minimalen Windows-Service Pack, die für eine Windows Installer Version erforderlich sind, finden Sie in den [Windows Installer Run-Time Anforderungen](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften](properties.md)
</dt> </dl>

 

 




