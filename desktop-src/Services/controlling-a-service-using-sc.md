---
description: Die Windows SDK enthält ein Befehlszeilen-Hilfsprogramm, Sc.exe, das zum Steuern eines Dienstanbieter verwendet werden kann. Die zugehörigen Befehle entsprechen den Funktionen, die vom SCM bereitgestellt werden. Die Syntax lautet wie folgt.
ms.assetid: 7c3e5c39-ec0f-4174-9ecf-239927de3d39
title: Steuern eines Dienstanbieter mit SC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c1aa991395ba2aa55bf05d63176fba59d96dce8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106359462"
---
# <a name="controlling-a-service-using-sc"></a>Steuern eines Dienstanbieter mit SC

Die Windows SDK enthält ein Befehlszeilen-Hilfsprogramm, Sc.exe, das zum Steuern eines Dienstanbieter verwendet werden kann. Die zugehörigen Befehle entsprechen den Funktionen, die vom SCM bereitgestellt werden. Die Syntax lautet wie folgt.

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

<dl> <dd>continue</dd> <dd>Steuerung</dd> <dd>abzufragen</dd> <dd>pause</dd> <dd>start</dd> <dd>stop</dd> </dl> </dd> <dt>

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

[Dienst Steuerungsanforderungen](service-control-requests.md)
</dt> <dt>

[Dienst Start](service-startup.md)
</dt> </dl>

 

 



