---
description: Die vorab ausgewählte Eigenschaft gibt an, dass bereits Features ausgewählt wurden und dass das Auswahl Dialogfeld nicht angezeigt werden muss. Bedingte Ausdrücke, die davon abhängen, ob Features bereits installiert sind, verwenden diesen Wert.
ms.assetid: 2bbab8b9-084a-4515-904c-d556d183d06e
title: Vorab ausgewählte Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 369a6d5fe7db99fab0032ee933afdb54bdb87efc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361422"
---
# <a name="preselected-property"></a>Vorab ausgewählte Eigenschaft

Die **vorab ausgewählte** Eigenschaft gibt an, dass bereits Features ausgewählt wurden und dass das Auswahl Dialogfeld nicht angezeigt werden muss.

Bedingte Ausdrücke, die davon abhängen, ob Features bereits installiert sind, verwenden diesen Wert. Beispielsweise kann die-Eigenschaft verwendet werden, um alle Dialogfelder zu unterdrücken, die während der Wiederaufnahme einer angehaltenen Installation die Funktionsauswahl betreffen.

Der Installer legt die **vorab ausgewählte** Eigenschaft während der Wiederaufnahme einer angehaltenen Installation auf den Wert "1" fest, oder wenn eine der folgenden Eigenschaften in der Befehlszeile angegeben wird. Wenn die **vorab ausgewählte** Eigenschaft auf 1 festgelegt wurde, verwendet das Installationsprogramm die Bedingungs [Tabelle](condition-table.md) nicht, um die Auswahl der Features auszuwerten. Funktionen werden basierend auf den folgenden Eigenschaften installiert. Das Installationsprogramm wertet diese Eigenschaften immer in der folgenden Reihenfolge aus:

1.  [**ADDLOCAL**](addlocal.md)
2.  [**Aufgeh**](remove.md)
3.  [**Addsource**](addsource.md)
4.  [**Adddefault**](adddefault.md)
5.  [**Installieren Sie**](reinstall.md)
6.  [**Benen**](advertise.md)
7.  [**Compaddlocal**](compaddlocal.md)
8.  [**Compaddsource**](compaddsource.md)
9.  [**Compadddefault**](compadddefault.md)
10. [**Fileaddlocal**](fileaddlocal.md)
11. [**Fileaddsource**](fileaddsource.md)
12. [**Fileadddefault**](fileadddefault.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer unter Windows Server 2003 oder Windows XP. Informationen zu den minimalen Windows-Service Pack, die für eine Windows Installer Version erforderlich sind, finden Sie in den [Windows Installer Run-Time Anforderungen](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften](properties.md)
</dt> </dl>

 

 




