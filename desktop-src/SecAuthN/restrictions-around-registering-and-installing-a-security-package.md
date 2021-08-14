---
description: Aktionen von Sicherheitspaketen, die in der Anwendung nicht Windows.
ms.assetid: E2BF8041-DF2F-4282-A3CC-A15FF2D7F4A2
title: Einschränkungen beim Registrieren und Installieren eines Sicherheitspakets
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dce9f2d81a0a724d232e39c6e6fd7565b946ca319ba9f134041f6865b4bb2450
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118918906"
---
# <a name="restrictions-around-registering-and-installing-a-security-package"></a>Einschränkungen beim Registrieren und Installieren eines Sicherheitspakets

Das Entfernen, Ersetzen oder Umschließen von Posteingangssicherheitspaketen (z. B. Kerberos oder NTLM) wird in Windows nicht unterstützt, und ab dem 10. Januar 2017 wird dies verhindert. Sicherheitspakete von Drittanbietern (SSPs/APs) können hinzugefügt werden. Allerdings unterstützt Windows das Entfernen vorkonfigurierten SSPs/APs nicht. Insbesondere das Bearbeiten der **Registrierungseinstellung HKLM \\ SYSTEM \\ CurrentControlSet \\ Control \\ Lsa \\ OSConfig Security \\ Packages** wurde nie unterstützt.

Ab Windows 8.1 können Kunden, die zusätzliche Funktionen bereitstellen möchten, ihre Sicherheitspakete mithilfe der Registrierungseinstellung **HKLM \\ SYSTEM \\ CurrentControlSet \\ Control \\ Lsa Security \\ Packages** ([Registering SSP/AP DLLs)](registering-ssp-ap-dlls.md)und der zugehörigen Registrierungseinstellung SecurityProviders ([Writing and Installing a Security Support Provider](writing-and-installing-a-security-support-provider.md)) (Schreiben und Installieren eines Sicherheitssupportanbieters) hinzufügen.  Darüber hinaus besteht der Zweck von  [Sicherheitspaketen](../secgloss/s-gly.md#_security_security_package_gly) in der Implementierung neuer Sicherheitsprotokolle, die in Form eines Sicherheitssupportanbieters (Security Support Provider, SSP) oder eines Authentifizierungspakets [(AP)](../secgloss/a-gly.md#_security_authentication_package_gly) verwendet werden können. Der Zweck eines SSP besteht im Bereitstellen authentifizierter  Verbindungs-, Nachrichtenintegritäts- und Nachrichtenverschlüsselungsdienste, die nicht  bereits im System unterstützt werden, während ein AP verwendet wird, um eine neue Authentifizierungslogik hinzuzufügen, die verwendet wird, um zu bestimmen, ob ein Benutzer sich anmelden darf. 

Microsoft investiert in die Kundensicherheit und versucht sicherzustellen, dass wichtige Prozesse wie SSPs und APs nicht einfach aus dem System austauschbar sind. Daher wurde die **Registrierungseinstellung HKLM \\ SYSTEM \\ CurrentControlSet \\ Control \\ Lsa \\ OSConfig Security \\ Packages** ab Windows 8.1 eingeschränkt, um Änderungen daran zu verhindern. Zur Vereinfachung von Sicherheitspaketen von Drittanbietern wurde **HKLM \\ SYSTEM \\ CurrentControlSet \\ Control \\ Lsa Security \\ Packages** zur festgelegten Einstellung für benutzerdefinierte SSPs/APs gemacht. Darüber hinaus wird empfohlen, alle Funktionen in benutzerdefinierten SSPs/APs, die außerhalb des von Microsoft definierten Bereichs von Sicherheitspaketen liegen, aus solchen benutzerdefinierten SSPs/APs zu entfernen, und dass Posteingangssicherheitspakete von keinen Produkten entfernt werden.

 

 
