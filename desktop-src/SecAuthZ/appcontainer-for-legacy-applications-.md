---
description: Die appcontainer-Umgebung ist eine restriktive Prozess Ausführungsumgebung, die für Legacy Anwendungen zum Bereitstellen von Ressourcensicherheit verwendet werden kann.
ms.assetid: 28498D4E-DCA4-4A85-B474-C3C328BD3022
title: Appcontainer für Legacy Anwendungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 269b25ea292bdb8935375e50f669d17deb7efaef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106373367"
---
# <a name="appcontainer-for-legacy-applications"></a>Appcontainer für Legacy Anwendungen

Die appcontainer-Umgebung ist eine restriktive Prozess Ausführungsumgebung, die für Legacy Anwendungen zum Bereitstellen von Ressourcensicherheit verwendet werden kann. Eine Anwendung, die in einem appcontainer ausgeführt wird, kann nur auf Ressourcen zugreifen, die Ihnen explizit zugewiesen sind. Folglich können Anwendungen, die in einem appcontainer implementiert werden, nicht gehackt werden, um böswillige Aktionen außerhalb der beschränkten zugewiesenen Ressourcen zuzulassen.

## <a name="benefits-of-using-an-appcontainer-environment"></a>Vorteile der Verwendung einer appcontainer-Umgebung

Die appcontainer-Umgebung bietet ein sicheres Sandkasten von Anwendungen. Dadurch wird die Anwendung nicht mehr auf Hardware, Dateien, Registrierung, andere Anwendungen, Netzwerk Konnektivität und Netzwerkressourcen zugreifen, ohne dass Sie über eine bestimmte Berechtigung verfügen. Einzelne Ressourcen können ohne verfügbar machen anderer Ressourcen als Ziel eingesetzt werden. Außerdem wird die Benutzeridentität durch eine eindeutige Identität geschützt, bei der es sich um eine Verkettung des Benutzers handelt, und die APP und die Ressourcen werden mithilfe eines Modells mit geringsten Rechten erteilt. Dadurch wird der Zugriff auf andere Ressourcen durch eine APP, die die Identität des Benutzers annimmt, weiter geschützt.

Weitere Informationen zur Verwendung von appcontainer für ältere Anwendungen finden Sie in den folgenden Themen.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                       | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                        |
|-----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Appcontainer-Isolation](appcontainer-isolation.md)<br/>             | Isolation ist das primäre Ziel einer appcontainer-Ausführungsumgebung. Wenn Sie eine Anwendung von nicht benötigten Ressourcen und anderen Anwendungen isolieren, werden Möglichkeiten für böswillige Manipulationen minimiert. Durch das Gewähren von Zugriff auf der Grundlage der geringsten Rechte wird verhindert, dass Anwendungen und Benutzer über ihre Rechte auf Ressourcen zugreifen. Das Steuern des Zugriffs auf Ressourcen schützt den Prozess, das Gerät und das Netzwerk.<br/> |
| [Implementieren eines appcontainer](implementing-an-appcontainer.md)<br/> | Ein appcontainer wird implementiert, indem dem Prozess Token neue Informationen hinzugefügt werden, wobei [**seaccesscheck ()**](/windows-hardware/drivers/ddi/content/wdm/nf-wdm-seaccesscheck) so geändert wird, dass alle veralteten, nicht geänderten Zugriffs Steuerungs Listen (ACL-Objekte) Zugriffs Anforderungen von appcontainer-Prozessen standardmäßig blockieren, sowie für appcontainers verfügbare reacl-Objekte.<br/>                                                                                        |



 

 

