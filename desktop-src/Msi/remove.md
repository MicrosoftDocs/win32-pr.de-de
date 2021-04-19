---
description: Der Wert der Remove-Eigenschaft ist eine Liste von Funktionen, die durch Kommas getrennt sind, die entfernt werden sollen.
ms.assetid: 39f4609a-7bf8-42b3-b23e-0d6a40b69fd3
title: REMOVE-Eigenschaft
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8f46bcd5547abdefd67f98dff312bfdf1dff41e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359788"
---
# <a name="remove-property"></a>REMOVE-Eigenschaft

Der Wert der **Remove** -Eigenschaft ist eine Liste von Funktionen, die durch Kommas getrennt sind, die entfernt werden sollen. Die Funktionen müssen in der featurespalte der [Funktions Tabelle](feature-table.md)vorhanden sein. Beachten Sie Folgendes: Wenn Sie "Remove = All" in der Befehlszeile verwenden, entfernt das Installationsprogramm alle Features, deren Installations Ebene größer als 0 ist. In diesem Fall entfernt das Installationsprogramm keine Features, die den Installations Grad 0 aufweisen. Weitere Informationen zur Installations Ebene der Features finden Sie unter [Featuretabelle](feature-table.md).

## <a name="remarks"></a>Bemerkungen

Um zu ermitteln, ob ein Produkt vollständig deinstalliert wurde, kann ein Paket Autor einen bedingten Ausdruck verwenden, um zu überprüfen, ob Remove = All. Beachten Sie Folgendes: Wenn das Produkt durch Festlegen seines Top-Features auf "Missing" entfernt wird, ist die **Remove** -Eigenschaft möglicherweise erst nach der [InstallValidate-Aktion](installvalidate-action.md)gleich. Dies bedeutet, dass alle benutzerdefinierten Aktionen, die von Remove = All abhängen, nach der InstallValidate sequenziert werden müssen. Weitere Informationen finden Sie auch [im Rahmen](conditioning-actions-to-run-during-removal.md)der Durchsetzung auszuführenden Anlagen Aktionen. Beachten Sie, dass die Funktionsnamen die Groß-/Kleinschreibung beachten.

Das Installationsprogramm wertet die folgenden Eigenschaften immer in der folgenden Reihenfolge aus:

1.  [**ADDLOCAL**](addlocal.md)
2.  **Aufgeh**
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

Wenn die Befehlszeile z. b. ADDLOCAL = ALL, addsource = myfeature angibt, werden alle Features zuerst auf Run-Local festgelegt, und myfeature wird auf Run-From-Source festgelegt. Wenn die Befehlszeile addsource = all, ADDLOCAL = myfeature, First myfeature auf Run-Local festgelegt ist, dann werden bei der Auswertung von addsource = All alle Funktionen (einschließlich myfeature) auf Run-From-Source zurückgesetzt.

Der Installer legt die [**vorab ausgewählte**](preselected.md) Eigenschaft während der Wiederaufnahme einer angehaltenen Installation auf den Wert "1" fest, oder wenn eine der oben aufgeführten Eigenschaften in der Befehlszeile angegeben wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer unter Windows Server 2003 oder Windows XP. Informationen zu den minimalen Windows-Service Pack, die für eine Windows Installer Version erforderlich sind, finden Sie in den [Windows Installer Run-Time Anforderungen](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften](properties.md)
</dt> </dl>

 

 




