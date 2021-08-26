---
description: Die Preselected -Eigenschaft gibt an, dass Features bereits ausgewählt wurden und dass das Auswahldialogfeld nicht angezeigt werden muss. Bedingte Ausdrücke, die davon abhängen, ob Features bereits installiert sind, verwenden diesen Wert.
ms.assetid: 2bbab8b9-084a-4515-904c-d556d183d06e
title: Vorab ausgewählte Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a85f5c3248002fec776e45e9d7ad37550d3e16d7a5d76b098948b571b8c9c546
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120042320"
---
# <a name="preselected-property"></a>Vorab ausgewählte Eigenschaft

Die **Preselected** -Eigenschaft gibt an, dass Features bereits ausgewählt wurden und dass das Auswahldialogfeld nicht angezeigt werden muss.

Bedingte Ausdrücke, die davon abhängen, ob Features bereits installiert sind, verwenden diesen Wert. Beispielsweise kann die -Eigenschaft verwendet werden, um alle Dialoge zu unterdrücken, die funktionsauswahl während der Wiederaufnahme einer angehaltenen Installation betreffen.

Das Installationsprogramm legt die **Preselected-Eigenschaft** während der Wiederaufnahme einer angehaltenen Installation oder wenn eine der folgenden Eigenschaften in der Befehlszeile angegeben wird, auf den Wert "1" fest. Wenn die **Preselected-Eigenschaft** auf 1 festgelegt wurde, verwendet das Installationsprogramm die [Tabelle Bedingung](condition-table.md) nicht, um die Auswahl der Features auszuwerten. Features werden basierend auf den folgenden Eigenschaften installiert. Das Installationsprogramm wertet diese Eigenschaften immer in der folgenden Reihenfolge aus:

1.  [**ADDLOCAL**](addlocal.md)
2.  [**Entfernen**](remove.md)
3.  [**ADDSOURCE**](addsource.md)
4.  [**ADDDEFAULT**](adddefault.md)
5.  [**Installieren**](reinstall.md)
6.  [**Werben**](advertise.md)
7.  [**COMPADDLOCAL**](compaddlocal.md)
8.  [**COMPADDSOURCE**](compaddsource.md)
9.  [**COMPADDDEFAULT**](compadddefault.md)
10. [**FILEADDLOCAL**](fileaddlocal.md)
11. [**FILEADDSOURCE**](fileaddsource.md)
12. [**FILEADDDEFAULT**](fileadddefault.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installationsprogramm 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installationsprogramm auf Windows Server 2003 oder Windows XP. Informationen zu den Windows Service [Pack-Mindestanforderungen,](windows-installer-portal.md) die für eine Windows Installer-Version erforderlich sind, finden Sie unter Run-Time Anforderungen für Windows Installer.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften](properties.md)
</dt> </dl>

 

 




