---
Description: Die Eigenschaft ALLUSERS konfiguriert den Installations Kontext des Pakets.
ms.assetid: 942e7764-a80f-4880-9559-72174f1827f7
title: ALLUSERS (Eigenschaft)
ms.topic: reference
ms.custom: snippet-project
ms.date: 07/27/2020
ms.openlocfilehash: f4e490216a16b6ef36cdb90efebbbf24a7b1b9cf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354733"
---
# <a name="allusers-property"></a>ALLUSERS (Eigenschaft)

Die Eigenschaft **ALLUSERS** konfiguriert den Installations Kontext des Pakets. Der Windows Installer führt eine Installation pro Benutzer oder eine Computer spezifische Installation durch, abhängig von den Zugriffsrechten des Benutzers, davon, ob für die Installation der Anwendung erhöhte Rechte erforderlich sind, den Wert der Eigenschaft " **ALLUSERS** ", den Wert der Eigenschaft " [**msiinstallperuser**](msiinstallperuser.md) " und die Version des Betriebssystems.

Der Wert der **ALLUSERS** -Eigenschaft bestimmt beim Installations Zeitpunkt den [Installations Kontext](installation-context.md).

-   Der Wert 1 der **ALLUSERS** -Eigenschaft gibt den Installations Kontext pro Computer an.
-   Ein **ALLUSERS** -Eigenschafts Wert einer leeren Zeichenfolge ("") gibt den Installations Kontext pro Benutzer an.
-   Wenn der Wert der Eigenschaft " **ALLUSERS** " auf 2 festgelegt ist, setzt der Windows Installer den Wert der Eigenschaft " **ALLUSERS** " immer auf "1" zurück und führt eine Installation pro Computer aus, oder der Wert der Eigenschaft " **ALLUSERS** " wird auf eine leere Zeichenfolge ("") zurückgesetzt, und es wird eine benutzerspezifische Installation durchführt. Der Wert ALLUSERS = 2 ermöglicht dem System, den Wert von **ALLUSERS** und den Installations Kontext zurückzusetzen, abhängig von den Berechtigungen des Benutzers und der Windows-Version.

    **Windows 7:** Legen Sie die Eigenschaft " **ALLUSERS** " auf "2" fest, um mithilfe der Eigenschaft " [**msiinstallperuser**](msiinstallperuser.md) " den Installations Kontext anzugeben. Legen Sie die **msiinstallperuser** -Eigenschaft für eine Computer spezifische Installation auf eine leere Zeichenfolge ("") fest. Legen Sie für eine Installation pro Benutzer die **msiinstallperuser** -Eigenschaft auf 1 fest. Wenn das Paket nach den in der [Erstellung eines einzelnen Pakets](single-package-authoring.md)beschriebenen Entwicklungs Richtlinien geschrieben wurde, können Benutzer mit Benutzer Zugriff im kontextbezogenen Kontext installieren, ohne UAC-Anmelde Informationen angeben zu müssen. Wenn der Benutzer über Benutzer Zugriffsberechtigungen verfügt, führt das Installationsprogramm nur dann eine Computer spezifische Installation aus, wenn im UAC-Dialogfeld die Administrator Anmelde Informationen bereitgestellt werden.

    **Windows Vista:** Legen Sie die Eigenschaft **ALLUSERS** auf 2 fest, und Windows Installer entspricht der [*Benutzerkontensteuerung (User Account Control*](u-gly.md) , UAC). Wenn der Benutzer über Benutzer Zugriffsberechtigungen und ALLUSERS = 2 verfügt, führt das Installationsprogramm nur dann eine Computer spezifische Installation aus, wenn im UAC-Dialogfeld die Administrator Anmelde Informationen bereitgestellt werden. Wenn die Benutzerkontensteuerung aktiviert ist und die richtigen Administrator Anmelde Informationen nicht bereitgestellt werden, tritt bei der Installation ein Fehler auf, der besagt, dass Administratorrechte erforderlich sind. Wenn die UAC durch den Registrierungsschlüssel, die Gruppenrichtlinie oder die Systemsteuerung deaktiviert ist, wird das Dialogfeld UAC nicht angezeigt, und bei der Installation tritt ein Fehler mit dem Hinweis auf, dass Administratorrechte erforderlich sind.

    **Windows XP:** Legen Sie die Eigenschaft " **ALLUSERS** " auf 2 fest, und Windows Installer führt eine Installation pro Benutzer aus, wenn der Benutzer über Benutzer Zugriffsberechtigungen verfügt.

-   Wenn der Wert der **ALLUSERS** -Eigenschaft nicht gleich 2 ist, ignoriert der Windows Installer den Wert der [**msiinstallperuser**](msiinstallperuser.md) -Eigenschaft.

## <a name="example"></a>Beispiel

```xml
  <!-- Disallow user from installing for all users -->
    <Property Id="ALLUSERS" Secure="yes"/>
    <Condition Message="Setting the ALLUSERS property is not allowed because [ProductName] is a per-user application. Setup will now exit.">
      NOT ALLUSERS
    </Condition>
```

Beispiel aus [klassischen Windows-Beispielen](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/DesktopToasts/CPP/Product.wxs) auf GitHub.

## <a name="default-value"></a>Standardwert

Der empfohlene Standard Installations Kontext ist pro Benutzer. Wenn **ALLUSERS** nicht festgelegt ist, führt das Installationsprogramm eine Installation pro Benutzer aus. Sie können sicherstellen, dass die Eigenschaft " **ALLUSERS** " nicht festgelegt wurde, indem Sie Ihren Wert auf eine leere Zeichenfolge (""), ALLUSERS = "" festlegen.

## <a name="remarks"></a>Bemerkungen

Der [Installations Kontext](installation-context.md) bestimmt die Werte der Eigenschaften [**DesktopFolder**](desktopfolder.md), [**ProgramMenuFolder**](programmenufolder.md), [**StartMenuFolder**](startmenufolder.md), [**startupfolder**](startupfolder.md), [**templatefolder**](templatefolder.md), [**admintoolsfolder**](admintoolsfolder.md), [**ProgramFilesFolder**](programfilesfolder.md), [**CommonFilesFolder**](commonfilesfolder.md), [**ProgramFiles64Folder**](programfiles64folder.md)und [**CommonFiles64Folder**](commonfiles64folder.md) . Der Installations Kontext bestimmt die Teile der Registrierung, in denen Einträge in der [Registrierungs Tabelle](registry-table.md) und der [removeregistry-Tabelle](removeregistry-table.md)mit-1 in der Stamm Spalte geschrieben oder entfernt werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer unter Windows Server 2003 oder Windows XP. Informationen zu den minimalen Windows-Service Pack, die für eine Windows Installer Version erforderlich sind, finden Sie in den [Windows Installer Run-Time Anforderungen](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften](properties.md)
</dt> <dt>

[**Msiinstallperuser**](msiinstallperuser.md)
</dt> <dt>

[Installations Kontext](installation-context.md)
</dt> <dt>

[Erstellung eines einzelnen Pakets](single-package-authoring.md)
</dt> </dl>

 

 




