---
description: Die Windows SDK enthält ein Befehlszeilen-Hilfsprogramm, Sc.exe, das zum Abfragen oder Ändern der Datenbank der installierten Dienste verwendet werden kann. Die zugehörigen Befehle entsprechen den Funktionen, die vom SCM bereitgestellt werden. Die Syntax lautet wie folgt.
ms.assetid: d304922c-86fb-4c62-9bfa-c827df4aecd8
title: Konfigurieren eines Dienstanbieter mit SC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f65669a3a7daa7e0d02731e6423adfbb3806f11
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348970"
---
# <a name="configuring-a-service-using-sc"></a>Konfigurieren eines Dienstanbieter mit SC

Die Windows SDK enthält ein Befehlszeilen-Hilfsprogramm, Sc.exe, das zum Abfragen oder Ändern der Datenbank der installierten Dienste verwendet werden kann. Die zugehörigen Befehle entsprechen den Funktionen, die vom SCM bereitgestellt werden. Die Syntax lautet wie folgt.

## <a name="syntax"></a>Syntax

**SC** \[ *Servername* \] *Befehl* \[ *Dienst Name* \] \[  \] Option1 \[ *Option2* \] ...

<dl> <dt>

<span id="ServerName"></span><span id="servername"></span><span id="SERVERNAME"></span>*Servername*
</dt> <dd>

Optionaler Servername. Verwenden Sie das Formular \\ \\ *Servername*.

</dd> <dt>

<span id="Command"></span><span id="command"></span><span id="COMMAND"></span>*S*
</dt> <dd>

Einer der folgenden Befehle:

<dl> <dd>starten</dd> <dd>config</dd> <dd>create</dd> <dd>delete</dd> <dd>description</dd> <dd>Enumabhängig</dd> <dd>failure</dd> <dd>failureflag</dd> <dd>GetDisplayName</dd> <dd>Getkeyname</dd> <dd>Sperre</dd> <dd>qc</dd> <dd>qdescription</dd> <dd>qfailure</dd> <dd>qfailureflag</dd> <dd>qprivs</dd> <dd>qsidtype</dd> <dd>Abfrage</dd> <dd>QUERYEX</dd> <dd>privs</dd> <dd>QueryLock</dd> <dd>Sdset</dd> <dd>sdshow</dd> <dd>showsid</dd> <dd>SIDType</dd> </dl> </dd> <dt>

<span id="ServiceName"></span><span id="servicename"></span><span id="SERVICENAME"></span>*Service Name*
</dt> <dd>

Der Name des Dienstanbieter, der bei der Installation angegeben wurde.

</dd> <dt>

<span id="option1"></span><span id="OPTION1"></span>*Option1*
</dt> <dd>

Ein optionaler Parameter.

</dd> <dt>

<span id="option2"></span><span id="OPTION2"></span>*Option2*
</dt> <dd>

Ein optionaler Parameter.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Verwenden Sie den folgenden Befehl, um die umfassende Syntax für einen Befehl anzuzeigen:

**SC** - *Befehl*

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Dienstkonfiguration:](service-configuration.md)
</dt> <dt>

[Dienst Installation, Entfernung und Enumeration](service-installation-removal-and-enumeration.md)
</dt> </dl>

 

 



