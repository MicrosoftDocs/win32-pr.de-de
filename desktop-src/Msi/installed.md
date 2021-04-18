---
description: Die installierte Eigenschaft wird nur festgelegt, wenn das Produkt pro Computer oder für den aktuellen Benutzer installiert ist.
ms.assetid: 139a6324-58fb-485e-8b3e-c5cf2881d5d1
title: Installierte Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ae5126107fff51f3790fb3ab9a9209490b9627a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358648"
---
# <a name="installed-property"></a>Installierte Eigenschaft

Die **installierte** Eigenschaft wird nur festgelegt, wenn das Produkt pro Computer oder für den aktuellen Benutzer installiert ist. Diese Eigenschaft ist nicht festgelegt, wenn das Produkt für einen anderen Benutzer installiert ist.

Die **installierte** Eigenschaft kann in bedingten Ausdrücken verwendet werden, um zu bestimmen, ob ein Produkt pro Computer oder für den aktuellen Benutzer installiert ist. Beispielsweise kann die-Eigenschaft in der Bedingungs Spalte einer Sequenz Tabelle oder zur Unterscheidung zwischen einer ersten Installation und einer Wartungs Installation verwendet werden.

Überprüfen Sie die Eigenschaft [**productstate**](productstate.md) , um zu bestimmen, ob das Produkt für einen anderen Benutzer installiert ist.

Der Wert der [**ProductVersion**](productversion.md) -Eigenschaft ist die Version des Produkts im Zeichen folgen Format.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer unter Windows Server 2003 oder Windows XP. Informationen zu den minimalen Windows-Service Pack, die für eine Windows Installer Version erforderlich sind, finden Sie in den [Windows Installer Run-Time Anforderungen](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften](properties.md)
</dt> </dl>

 

 




