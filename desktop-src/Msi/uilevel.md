---
description: Der Installer legt die uilevel-Eigenschaft auf die Ebene der Benutzeroberfläche fest.
ms.assetid: 9fc58026-f140-4218-b44f-50fc6b0ef3e9
title: Uilevel-Eigenschaft
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83b48ebaeb246f42e552b93c974db92c78e54dbc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368524"
---
# <a name="uilevel-property"></a>Uilevel-Eigenschaft

Der Installer legt die **uilevel** -Eigenschaft auf die Ebene der Benutzeroberfläche fest. Die interne Benutzeroberfläche wird von [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui)aktiviert und festgelegt. Diese Eigenschaft wird auf einen der folgenden installuilevel-Datentypen festgelegt.



| Installuilevel          | Numerischer Wert | Benutzeroberflächen Ebene                        |
|-------------------------|---------------|---------------------------------------------|
| installuilevel \_ None    | 2             | Vollständig automatische Installation:             |
| installuilevel \_ Basic   | 3             | Einfacher Fortschritt und Fehlerbehandlung.         |
| installuilevel \_ reduziert | 4             | Erstellte Benutzeroberfläche, Assistenten Dialogfelder werden unterdrückt.     |
| installuilevel \_ voll    | 5             | Erstellte Benutzeroberfläche mit Assistenten, Fortschritt, Fehlern. |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer unter Windows Server 2003 oder Windows XP. Informationen zu den minimalen Windows-Service Pack, die für eine Windows Installer Version erforderlich sind, finden Sie in den [Windows Installer Run-Time Anforderungen](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften](properties.md)
</dt> <dt>

[Benutzeroberfläche](user-interface.md)
</dt> <dt>

[Bestimmen der Benutzeroberflächen Ebene aus einer benutzerdefinierten Aktion](determining-ui-level-from-a-custom-action.md)
</dt> </dl>

 

 




