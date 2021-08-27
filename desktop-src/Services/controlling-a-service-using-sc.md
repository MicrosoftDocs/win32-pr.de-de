---
description: Das Windows SDK enthält ein Befehlszeilenprogramm Sc.exe, das zum Steuern eines Diensts verwendet werden kann. Die Befehle entsprechen den vom SCM bereitgestellten Funktionen. Die Syntax lautet wie folgt.
ms.assetid: 7c3e5c39-ec0f-4174-9ecf-239927de3d39
title: Steuern eines Diensts mit sc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2481e0d13f19760c042d39efe4ec6094a3ef270312aeb31d2228d401d914bc1f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120126450"
---
# <a name="controlling-a-service-using-sc"></a>Steuern eines Diensts mit sc

Das Windows SDK enthält ein Befehlszeilenprogramm Sc.exe, das zum Steuern eines Diensts verwendet werden kann. Die Befehle entsprechen den vom SCM bereitgestellten Funktionen. Die Syntax lautet wie folgt.

## <a name="syntax"></a>Syntax

**sc** \[ *ServerName* \] *Befehl* \[ *ServiceName* \] \[ *option1* \] \[ *option2* \] ...

<dl> <dt>

<span id="ServerName"></span><span id="servername"></span><span id="SERVERNAME"></span>*Servername*
</dt> <dd>

Optionaler Servername. Verwenden Sie das Format \\ \\ *ServerName*.

</dd> <dt>

<span id="Command"></span><span id="command"></span><span id="COMMAND"></span>*Befehl*
</dt> <dd>

Einer der folgenden Befehle:

<dl> <dd>continue</dd> <dd>Steuerung</dd> <dd>Abfragen</dd> <dd>pause</dd> <dd>start</dd> <dd>stop</dd> </dl> </dd> <dt>

<span id="ServiceName"></span><span id="servicename"></span><span id="SERVICENAME"></span>*Servicename*
</dt> <dd>

Der Name des Diensts, wie bei der Installation angegeben.

</dd> <dt>

<span id="option1"></span><span id="OPTION1"></span>*option1*
</dt> <dd>

Ein optionaler Parameter.

</dd> <dt>

<span id="option2"></span><span id="OPTION2"></span>*option2*
</dt> <dd>

Ein optionaler Parameter.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Verwenden Sie den folgenden Befehl, um die vollständige Syntax für einen Befehl anzuzeigen:

**sc-Befehl** 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Dienststeuerungsanforderungen](service-control-requests.md)
</dt> <dt>

[Dienststart](service-startup.md)
</dt> </dl>

 

 



