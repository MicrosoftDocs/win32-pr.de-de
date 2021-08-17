---
description: Die Installed-Eigenschaft wird nur festgelegt, wenn das Produkt pro Computer oder für den aktuellen Benutzer installiert ist.
ms.assetid: 139a6324-58fb-485e-8b3e-c5cf2881d5d1
title: Installierte Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5925f68595f6b0975e64281be0ba7326fa831d08f0298f9b84375df97e5196c0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118633523"
---
# <a name="installed-property"></a>Installierte Eigenschaft

Die **Installed-Eigenschaft** wird nur festgelegt, wenn das Produkt pro Computer oder für den aktuellen Benutzer installiert ist. Diese Eigenschaft wird nicht festgelegt, wenn das Produkt für einen anderen Benutzer installiert ist.

Die **Installed-Eigenschaft** kann in bedingten Ausdrücken verwendet werden, um zu bestimmen, ob ein Produkt pro Computer oder für den aktuellen Benutzer installiert ist. Beispielsweise kann die -Eigenschaft in der bedingungsbedingten Spalte einer Sequenztabelle oder verwendet werden, um zwischen einer ersten Installation und einer Wartungsinstallation zu unterscheiden.

Überprüfen Sie die [**ProductState-Eigenschaft,**](productstate.md) um zu ermitteln, ob das Produkt für einen anderen Benutzer installiert ist.

Der Wert der [**ProductVersion-Eigenschaft**](productversion.md) ist die Version des Produkts im Zeichenfolgenformat.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installationsprogramm auf Windows Server 2003 oder Windows XP. Informationen zum [Windows Service](windows-installer-portal.md) Pack, das für eine Windows Installer-Version erforderlich ist, finden Sie unter Windows Installer Run-Time Anforderungen.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften](properties.md)
</dt> </dl>

 

 




