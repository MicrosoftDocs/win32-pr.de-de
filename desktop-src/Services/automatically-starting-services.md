---
description: Beim Systemstart startet der SCM alle automatischen Start Dienste und die Dienste, von denen Sie abhängig sind. Wenn z. b. ein Auto Start Dienst von einem Dienst zum Starten von Start abhängig ist, wird der Dienst für die Dienst Nachfrage ebenfalls automatisch gestartet.
ms.assetid: 8aa60e96-a35e-4670-832c-c045d0903618
title: Dienste werden automatisch gestartet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40b2e7ef0c65e72ee21145891b6f9598117a7afe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106340176"
---
# <a name="automatically-starting-services"></a>Dienste werden automatisch gestartet

Beim Systemstart startet der SCM alle automatischen Start Dienste und die Dienste, von denen Sie abhängig sind. Wenn z. b. ein Auto Start Dienst von einem Dienst zum Starten von Start abhängig ist, wird der Dienst für die Dienst Nachfrage ebenfalls automatisch gestartet.

Die Lade Reihenfolge wird durch Folgendes bestimmt:

1.  Die Reihenfolge der Gruppen in der Gruppenliste der Lade Reihenfolge. Diese Informationen werden im Wert " **servicegrouporder** " im folgenden Registrierungsschlüssel gespeichert:

    **HKEY \_ local \_ Machine \\ System \\ CurrentControlSet- \\ Steuerelement**

    Um die Gruppe der Lade Reihen für einen Dienst anzugeben, verwenden Sie den *lploadordergroup* - [**Parameter der Funktion**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) "Funktion" oder " [**ChangeServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfiga) ".

2.  Die Reihenfolge der Dienste innerhalb einer Gruppe, die im Bestellungs Vektor für Tags angegeben ist. Diese Informationen werden im folgenden Registrierungsschlüssel im **grouporderlist** -Wert gespeichert:

    **HKEY \_ local \_ Machine \\ System \\ CurrentControlSet- \\ Steuerelement**

3.  Die für jeden Dienst aufgelisteten Abhängigkeiten.

Nach Abschluss des Starts führt das System das Start Überprüfungs Programm aus, das vom Wert " **bootverificationprogram** " des folgenden Registrierungsschlüssels angegeben wird: **HKEY \_ local \_ Machine \\ System \\ CurrentControlSet \\ Control**.

Standardmäßig ist dieser Wert nicht festgelegt. Das System meldet einfach, dass der Start erfolgreich war, nachdem sich der erste Benutzer angemeldet hat. Sie können ein Start Überprüfungs Programm bereitstellen, das das System auf Probleme überprüft und den Startstatus mithilfe der [**notifybootconfigstatus**](/windows/desktop/api/Winsvc/nf-winsvc-notifybootconfigstatus) -Funktion an den SCM meldet.

Nach einem erfolgreichen Start speichert das System einen Klon der Datenbank in der Konfiguration mit den letzten bekannten Voreinstellungen. Das System kann diese Kopie der Datenbank wiederherstellen, wenn die an der aktiven Datenbank vorgenommenen Änderungen dazu führen, dass der Systemneustart fehlschlägt. Der Registrierungsschlüssel für diese Datenbank lautet wie folgt:

**Lokale HKEY- \_ \_ Computer- \\ \\ Controlset *xxx*- \\ Dienste**

Dabei ist *xxx* der Wert, der im folgenden Registrierungs Wert gespeichert wird: **HKEY \_ local \_ Machine \\ System \\ Select \\ LastKnownGood**.

Wenn ein automatischer Start Dienst mit einer \_ \_ Fehler Steuerungsebene des Dienst Fehlers nicht gestartet werden kann, startet der SCM den Computer mithilfe der LKG-Konfiguration neu. Wenn die LKG-Konfiguration bereits verwendet wird, tritt beim Starten ein Fehler auf.

Ein Dienst für automatisches Starten kann als verzögerter Dienst für automatisches Starten konfiguriert werden, indem die [**ChangeServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfig2a) -Funktion \_ mit \_ verzögerten \_ automatischen \_ Start \_ Informationen für die Dienst Konfiguration aufgerufen wird. Diese Änderung tritt nach dem nächsten Systemstart in Kraft. Weitere Informationen finden Sie unter [**Dienst \_ verzögerte \_ automatische \_ Start \_ Informationen**](/windows/desktop/api/Winsvc/ns-winsvc-service_delayed_auto_start_info).

 

 



