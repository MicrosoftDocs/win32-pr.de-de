---
Description: Die ALLUSERS-Eigenschaft konfiguriert den Installationskontext des Pakets.
ms.assetid: 942e7764-a80f-4880-9559-72174f1827f7
title: ALLUSERS-Eigenschaft
ms.topic: reference
ms.custom: snippet-project
ms.date: 07/27/2020
ms.openlocfilehash: b6412707d6ef46b55d1f8add3de56a24e6f970dc9fa7f0353dce6ec9efa9f531
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119581880"
---
# <a name="allusers-property"></a>ALLUSERS-Eigenschaft

Die **ALLUSERS-Eigenschaft** konfiguriert den Installationskontext des Pakets. Der Windows Installer führt eine Installation pro Benutzer oder pro Computer aus. Dies hängt von den Zugriffsberechtigungen des Benutzers ab, unabhängig davon, ob für die Installation der Anwendung erhöhte Rechte erforderlich sind, den Wert der **ALLUSERS-Eigenschaft,** den Wert der [**MSIINSTALLPERUSER-Eigenschaft**](msiinstallperuser.md) und die Version des Betriebssystems.

Der Wert der **ALLUSERS-Eigenschaft** bestimmt zur Installationszeit den [Installationskontext](installation-context.md).

-   Der **ALLUSERS-Eigenschaftswert** 1 gibt den Installationskontext pro Computer an.
-   Ein **ALLUSERS-Eigenschaftswert** einer leeren Zeichenfolge ("") gibt den Installationskontext pro Benutzer an.
-   Wenn der Wert der **ALLUSERS-Eigenschaft** auf 2 festgelegt ist, setzt der Windows Installer den Wert der **ALLUSERS-Eigenschaft** immer auf 1 zurück und führt eine Computerinstallation durch, oder der Wert der **ALLUSERS-Eigenschaft** wird auf eine leere Zeichenfolge ("") zurückgesetzt, und es wird eine Installation pro Benutzer durchgeführt. Mit dem Wert ALLUSERS=2 kann das System den Wert von **ALLUSERS** und den Installationskontext zurücksetzen, abhängig von den Berechtigungen des Benutzers und der Version von Windows.

    **Windows 7:** Legen Sie die **ALLUSERS-Eigenschaft** auf 2 fest, um den Installationskontext mithilfe der [**MSIINSTALLPERUSER-Eigenschaft**](msiinstallperuser.md) anzugeben. Legen Sie die **MSIINSTALLPERUSER-Eigenschaft** für eine Computerinstallation auf eine leere Zeichenfolge ("") fest. Legen Sie die **MSIINSTALLPERUSER-Eigenschaft** für eine Benutzerinstallation auf 1 fest. Wenn das Paket gemäß den Unter [Erstellen einzelner](single-package-authoring.md)Pakete beschriebenen Entwicklungsrichtlinien geschrieben wurde, können Benutzer mit Benutzerzugriff im Benutzerkontext installieren, ohne UAC-Anmeldeinformationen angeben zu müssen. Wenn der Benutzer über Benutzerzugriffsrechte verfügt, führt das Installationsprogramm nur dann eine Computerinstallation durch, wenn administratoranmeldeinformationen für das Dialogfeld "Benutzerkontenverwaltung" bereitgestellt werden.

    **Windows Vista:** Legen Sie die **ALLUSERS-Eigenschaft** auf 2 fest, und Windows Installer der Benutzerkontensteuerung (User [*Account Control,*](u-gly.md) UAC) entspricht. Wenn der Benutzer über Benutzerzugriffsberechtigungen und ALLUSERS=2 verfügt, führt das Installationsprogramm nur dann eine computerspezifische Installation durch, wenn Administratoranmeldeinformationen für das Dialogfeld benutzerkontenbasierte Zugriffsverwaltung bereitgestellt werden. Wenn die UAC aktiviert ist und die richtigen Administratoranmeldeinformationen nicht angegeben werden, tritt bei der Installation ein Fehler auf, der besagt, dass Administratorrechte erforderlich sind. Wenn die UAC durch den Registrierungsschlüssel, die Gruppenrichtlinie oder die Systemsteuerung deaktiviert ist, wird das UAC-Dialogfeld nicht angezeigt, und bei der Installation tritt ein Fehler auf, der besagt, dass Administratorrechte erforderlich sind.

    **Windows XP:** Legen Sie die **ALLUSERS-Eigenschaft** auf 2 fest, und Windows Installer eine Installation pro Benutzer ausführt, wenn der Benutzer über Benutzerzugriffsrechte verfügt.

-   Wenn der Wert der **ALLUSERS-Eigenschaft** nicht gleich 2 ist, ignoriert der Windows Installer den Wert der [**MSIINSTALLPERUSER-Eigenschaft.**](msiinstallperuser.md)

## <a name="example"></a>Beispiel

```xml
  <!-- Disallow user from installing for all users -->
    <Property Id="ALLUSERS" Secure="yes"/>
    <Condition Message="Setting the ALLUSERS property is not allowed because [ProductName] is a per-user application. Setup will now exit.">
      NOT ALLUSERS
    </Condition>
```

Beispiel aus [Windows klassischen Beispielen](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/DesktopToasts/CPP/Product.wxs) auf GitHub.

## <a name="default-value"></a>Standardwert

Der empfohlene Standardinstallationskontext ist pro Benutzer. Wenn **ALLUSERS** nicht festgelegt ist, führt das Installationsprogramm eine Installation pro Benutzer durch. Sie können sicherstellen, dass die **ALLUSERS-Eigenschaft** nicht festgelegt wurde, indem Sie ihren Wert auf eine leere Zeichenfolge (""), ALLUSERS="" festlegen.

## <a name="remarks"></a>Hinweise

Der [Installationskontext](installation-context.md) bestimmt die Werte der Eigenschaften [**DesktopFolder,**](desktopfolder.md) [**ProgramMenuFolder,**](programmenufolder.md) [**StartMenuFolder,**](startmenufolder.md) [**StartupFolder,**](startupfolder.md) [**TemplateFolder,**](templatefolder.md) [**AdminToolsFolder,**](admintoolsfolder.md) [**ProgramFilesFolder,**](programfilesfolder.md) [**CommonFilesFolder,**](commonfilesfolder.md) [**ProgramFiles64Folder**](programfiles64folder.md)und [**CommonFiles64Folder.**](commonfiles64folder.md) Der Installationskontext bestimmt die Teile der Registrierung, in denen Einträge in der [Registrierungstabelle](registry-table.md) und in der [RemoveRegistry-Tabelle](removeregistry-table.md)mit -1 in der Stammspalte geschrieben oder entfernt werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installationsprogramm 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installationsprogramm auf Windows Server 2003 oder Windows XP. Informationen zu den mindestens erforderlichen Windows Service Packs, die für eine Windows Installer-Version erforderlich sind, finden Sie unter Run-Time [Anforderungen](windows-installer-portal.md) für Windows Installer.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften](properties.md)
</dt> <dt>

[**MSIINSTALLPERUSER**](msiinstallperuser.md)
</dt> <dt>

[Installationskontext](installation-context.md)
</dt> <dt>

[Erstellen einzelner Pakete](single-package-authoring.md)
</dt> </dl>

 

 




