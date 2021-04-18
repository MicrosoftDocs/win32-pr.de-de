---
description: Die Eigenschaften msiinstallperuser und ALLUSERS können vom Benutzer zur Installationszeit, über die Benutzeroberfläche oder über die Befehlszeile festgelegt werden, um anzufordern, dass die Windows Installer ein Paket mit zwei Zweck für den aktuellen Benutzer oder alle Benutzer des Computers installieren.
ms.assetid: 17eb24e4-8464-4724-9768-4b58446ee4bc
title: Msiinstallperuser (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b3fa54026c859b5f4f610fd54aec2df3ca518ad4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106357559"
---
# <a name="msiinstallperuser-property"></a>Msiinstallperuser (Eigenschaft)

Die Eigenschaften **msiinstallperuser** und [**ALLUSERS**](allusers.md) können vom Benutzer zur Installationszeit, über die Benutzeroberfläche oder über die Befehlszeile festgelegt werden, um anzufordern, dass die Windows Installer ein Paket mit zwei Zweck für den aktuellen Benutzer oder alle Benutzer des Computers installieren. Um die **msiinstallperuser** -Eigenschaft verwenden zu können, muss der Wert der Eigenschaft " [**ALLUSERS**](allusers.md) " 2 sein, und das Paket muss erstellt worden sein, damit die Installation entweder im Benutzer-oder in einem computerbezogenen Kontext erfolgen kann. Informationen zum Erstellen eines Pakets mit zwei Zweck, finden Sie unter [Erstellen einzelner Pakete](single-package-authoring.md). Wenn der Wert der Eigenschaft " **ALLUSERS** " nicht gleich 2 ist, wird der Wert der Eigenschaft " **msiinstallperuser** " ignoriert und hat keine Auswirkung auf die Installation. Der Wert der **msiinstallperuser** -Eigenschaft wird bei der Installation des Pakets mit Windows Installer 4,5 oder früher ignoriert.

Der Benutzer kann den Wert der Eigenschaft " **msiinstallperuser** " auf eine leere Zeichenfolge ("") und den Wert der Eigenschaft " [**ALLUSERS**](allusers.md) " auf "2" [festlegen, indem](installation-context.md)er eine erstellte Benutzeroberfläche oder eine Befehlszeile verwendet. Windows Installer

Der Benutzer kann den Wert der Eigenschaft " **msiinstallperuser** " auf 1 und den Wert der Eigenschaft " [**ALLUSERS**](allusers.md) " auf "2" festlegen, indem er eine erstellte Benutzeroberfläche oder eine Befehlszeile verwendet, um anzufordern, dass der Windows Installer das Paket mit zwei Zweck im [Installations Kontext](installation-context.md)pro Benutzer installiert.

Wenn der Wert der [**ALLUSERS**](allusers.md) -Eigenschaft nicht gleich 2 ist, ignoriert der Windows Installer den Wert der **msiinstallperuser** -Eigenschaft. Wenn Windows Installer die Anwendung im computerspezifischen Kontext installiert, wird der Wert der Eigenschaft " **ALLUSERS** " auf 1 zurückgesetzt. Wenn Windows Installer die Anwendung im kontextbezogenen Kontext installiert, setzt Sie den Wert der **ALLUSERS** -Eigenschaft auf eine leere Zeichenfolge ("") zurück. Anwendungen, die pro Benutzer installiert wurden, erhalten daher alle Updates oder Reparaturen pro Benutzer, und pro Computer installierte Anwendungen erhalten Updates oder Reparaturen auf Computer Basis.

**[Windows Installer 4,5 oder früher](not-supported-in-windows-installer-4-5.md):** die **msiinstallperuser** -Eigenschaft wird von früheren Versionen als Windows Installer 5,0 ignoriert.

## <a name="default-value"></a>Standardwert

Der empfohlene Standard Installations Kontext ist pro Benutzer für ein Paket mit zwei Zweck. Erstellen Sie msiinstallperuser = 1 und ALLUSERS = 2 in der [Eigenschaften Tabelle](property-table.md) des Pakets mit zwei Zweck, um pro Benutzer als Standard Installations Kontext anzugeben.

## <a name="remarks"></a>Bemerkungen

Sie können sicherstellen, dass die **msiinstallperuser** -Eigenschaft nicht festgelegt wurde, indem Sie Ihren Wert auf eine leere Zeichenfolge (""), msiinstallperuser = "" festlegen.

Der Installations Kontext bestimmt die Werte der Eigenschaften [**DesktopFolder**](desktopfolder.md), [**ProgramMenuFolder**](programmenufolder.md), [**StartMenuFolder**](startmenufolder.md), [**startupfolder**](startupfolder.md), [**templatefolder**](templatefolder.md), [**admintoolsfolder**](admintoolsfolder.md), [**ProgramFilesFolder**](programfilesfolder.md), [**CommonFilesFolder**](commonfilesfolder.md), [**ProgramFiles64Folder**](programfiles64folder.md)und [**CommonFiles64Folder**](commonfiles64folder.md) . Der Installations Kontext bestimmt die Teile der Registrierung, in denen Einträge in der [Registrierungs Tabelle](registry-table.md) und der [removeregistry-Tabelle](removeregistry-table.md)mit-1 in der Stamm Spalte geschrieben oder entfernt werden. Weitere Informationen zum Installations Kontext finden Sie unter [Installations Kontext](installation-context.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Informationen zu den minimalen Windows-Service Pack, die für eine Windows Installer Version erforderlich sind, finden Sie in den [Windows Installer Run-Time Anforderungen](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften](properties.md)
</dt> <dt>

[**ALLUSERS**](allusers.md)
</dt> <dt>

[Installations Kontext](installation-context.md)
</dt> <dt>

[Erstellung eines einzelnen Pakets](single-package-authoring.md)
</dt> </dl>

 

 




